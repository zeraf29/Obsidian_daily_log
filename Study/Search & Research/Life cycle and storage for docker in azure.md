

--- 
author: zeraf29
created: 2023-09-20 19:32 
last-updated: 2023-09-20 19:32 
summaries: 
tags:

---


## Memo

You are developing an application that includes two Docker containers. The application must meet the following requirements: • The containers must not run as root. • The containers must be deployed to Azure Container Instances by using a YAML le. • The containers must share a lifecycle, resources, local network, and storage volume. • The storage volume must persist through container crashes. • The storage volume must be deployed on stop or restart of the containers. You need to congure Azure Container Instances for the application. Which conguration values should you use? To answer, select the appropriate shared lifecycle and storage volume options in the below options.

 Shared lifecycle: container group, container image, service endpoint, resource group 
 Storage volume: azure file share, secret, empty directory, clone git repo


The correct answers are:

**Shared lifecycle:** **container group** **Storage volume:** **empty directory**

**Explanation:**

- **Shared lifecycle:** The container group option will allow the two containers to share a lifecycle, resources, local network, and storage volume.
- **Storage volume:** The empty directory option will create a new empty directory on the host machine and mount it to the containers. This directory will persist through container crashes and will be deployed on stop or restart of the containers.

Azure file shares require root access to mount, so the Azure file share option is not compatible with the requirement that the containers must not run as root.

The secret and clone git repo options are not compatible with the requirement that the storage volume must persist through container crashes and must be deployed on stop or restart of the containers.

Here is an example of a YAML file that you can use to deploy the application to Azure Container Instances:

YAML

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: my-container
        image: my-container-image
        securityContext:
          runAsNonRoot: true
        volumeMounts:
        - name: my-volume
          mountPath: /my-volume
      volumes:
      - name: my-volume
        emptyDir: {}
```

코드를 사용할 때는 주의하시기 바랍니다. [자세히 알아보기](https://bard.google.com/faq#coding)

This will create a container group that includes two containers of the `my-container-image` image. The containers will share a lifecycle, resources, local network, and storage volume. The storage volume will be created as an empty directory on the host machine and will persist through container crashes and will be deployed on stop or restart of the containers. The containers will run as a non-root user, which meets the requirement that the containers must not run as root.

#### 출처

[](https://bard.google.com/faq#citation)

1. [newrelic.com/blog/how-to-relic/how-to-monitor-prometheus-metrics](https://newrelic.com/blog/how-to-relic/how-to-monitor-prometheus-metrics) 
    
2. [www.kubermatic.com/blog/introduction-to-kubernetes-replicasets/](https://www.kubermatic.com/blog/introduction-to-kubernetes-replicasets/)



**Secret volume**

Secret volumes are used to mount secrets, such as passwords, keys, and certificates, into containers. Secrets are stored in a secure encrypted format and are only accessible to the container that is mounted to.

Secret volumes cannot be used to persist data through container crashes or to deploy data on stop or restart of the containers. When a container crashes, the secret volume is unmounted and the data is lost. Similarly, when a container is stopped or restarted, the secret volume is unmounted and the data is lost.

**Clone git repo volume**

Clone git repo volumes are used to clone a Git repository into a container. The Git repository can be used to store the application code, configuration files, and other data.

Clone git repo volumes cannot be used to persist data through container crashes or to deploy data on stop or restart of the containers. When a container crashes, the clone git repo volume is unmounted and the data is lost. Similarly, when a container is stopped or restarted, the clone git repo volume is unmounted and the data is lost.

However, you can use a clone git repo volume to deploy the application code to the containers. You can do this by cloning the Git repository into a directory on the host machine and then mounting that directory to the containers using an empty directory volume.

Here is an example of how to deploy the application code to the containers using a clone git repo volume and an empty directory volume:

YAML

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: my-container
        image: my-container-image
        securityContext:
          runAsNonRoot: true
        volumeMounts:
          - name: my-volume
            mountPath: /my-volume
          - name: my-git-repo
            mountPath: /my-git-repo
      volumes:
      - name: my-volume
        emptyDir: {}
      - name: my-git-repo
        gitRepo:
          repository: https://github.com/my-organization/my-repo.git
```

코드를 사용할 때는 주의하시기 바랍니다. [자세히 알아보기](https://bard.google.com/faq#coding)

This will create a container group that includes two containers of the `my-container-image` image. The containers will share a lifecycle, resources, local network, and storage volume. The storage volume will be created as an empty directory on the host machine and will persist through container crashes and will be deployed on stop or restart of the containers. The containers will run as a non-root user, which meets the requirement that the containers must not run as root.

The Git repository will be cloned into the `/my-git-repo` directory on the host machine and will be mounted to the containers using the `my-git-repo` volume. The containers can then access the application code in the `/my-git-repo` directory.

I hope this explanation is helpful. Please let me know if you have any other questions.

#### 출처

[](https://bard.google.com/faq#citation)

1. [newrelic.com/blog/how-to-relic/how-to-monitor-prometheus-metrics](https://newrelic.com/blog/how-to-relic/how-to-monitor-prometheus-metrics) 
    
2. [www.kubermatic.com/blog/introduction-to-kubernetes-replicasets/](https://www.kubermatic.com/blog/introduction-to-kubernetes-replicasets/)