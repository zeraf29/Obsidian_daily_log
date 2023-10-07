
1. Question 1
	You have two Hyper-V hosts named Host1 and Host2. Host1 has an Azure virtual machine named VM1 that was deployed by using a custom Azure Resource  Manager template.  You need to move VM1 to Host2. What should you do?
	
	A. From the Update management blade, click Enable.  
	B. From the Overview blade, move VM1 to a different subscription.
	C. From the Redeploy blade, click Redeploy. 
	D. From the Profile blade, modify the usage location.
	
	- C. From the Redeploy blade, click Redeploy
	- When you redeploy a VM, it moves the VM to a new node within the Azure infrastructure and then powers it back on, retaining all your conguration options and associated resources.
	- 
2. Question 2
   You have downloaded an Azure Resource Manager template to deploy numerous virtual machines. The template is based on a current virtual machine, but must be adapted to reference an administrative password.  
   You need to make sure that the password is not stored in plain text.  
   You are preparing to create the necessary components to achieve your goal.   
   Which of the following should you create to achieve your goal? Answer by dragging the correct option from the list to the answer area.

	- Options
		- An Azure Key Vault
		- An Azure Storage Valut 
		- Azure Active Directory(AD) Identity Protection
		- An access policy
		- An Azure Policy
		- A Backup Policy
		  
	- An access policy, An Azure Key Vault
		- An Azure key Vault: Create a secret containing own password
		- An access policy: Allow access to the previously created secret 
		- -> Check more What are they exactly working

3. Your company has an Azure Kubernetes Service (AKS) cluster that you manage from an Azure AD-joined device. The cluster is located in a resource group.  
	Developers have created an application named MyApp. MyApp was packaged into a container image.  
	You need to deploy the YAML manifest file for the application.

	Solution: You install the Azure CLI on the device and run the `kubectl apply -f myapp.yaml` command.

	Does this meet the goal? 

	A. Yes
	B. No

	- Yes
		- kubectl apply -f myapp.yaml applies a conguration change to a resource from a file or stdin.

4. Your company has an Azure Kubernetes Service (AKS) cluster that you manage from an Azure AD-joined device. The cluster is located in a resource group.  
	Developers have created an application named MyApp. MyApp was packaged into a container image.  
	You need to deploy the YAML manifest file for the application.

	Solution: You install the docker client on the device and run the `docker run -it microsoft/azure-cli:0.10.17` command. 

	Does this meet the goal?

	A. Yes
	B. No

	- B. No
		- It's not Kubernetes command. It's Docker command
		- use the `kubectl` command

5. Your company has a web app named WebApp1.  
	You use the WebJobs SDK to design a triggered App Service background task that automatically invokes a function in the code every time new data is received in a queue.  
	You are preparing to configure the service processes a queue data item.  
	Which of the following is the service you should use?

	A. Logic Apps
	B. WebJobs
	C. Flow
	D. Functions

	- B. WebJobs

6. Your company has an Azure subscription.  
	You need to deploy a number of Azure virtual machines to the subscription by using Azure Resource Manager (ARM) templates. The virtual machines will be included in a single availability set.  
	You need to ensure that the ARM template allows for as many virtual machines as possible to remain accessible in the event of fabric failure or maintenance.  
	Which of the following is the value that you should configure for the platformFaultDomainCount property?

	A. 10
	B. 30
	C. Min Value
	D. Max Value

	- D. Max Value
		- 