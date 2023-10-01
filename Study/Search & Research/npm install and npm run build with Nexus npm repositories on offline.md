

--- 
author: zeraf29
created: 2023-09-19 10:17 
last-updated: 2023-09-19 10:17 
summaries: set NPM_CONFIG_REGISTRY for npm install and build with Nexus on offline
tags: npm, NPM_CONFIG_REGISTRY, Nexus

---
![photo by Yianni Mathioudakis on Unsplash](https://images.unsplash.com/photo-1692643667753-563480a3e952?crop=entropy&cs=srgb&fm=jpg&ixid=M3wzNjM5Nzd8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTUwODYyNzl8&ixlib=rb-4.0.3&q=85) 

## Memo
- To npm install and npm run build with Nexus npm repositories on an offline environment, you can follow these steps:

1. **Install Nexus.** You can install Nexus on any machine with access to the internet.
2. **Create a Nexus npm repository.** You can do this from the Nexus web interface.
3. **Download your dependencies to Nexus.** You can use the `npm install` command to download your dependencies to Nexus. To do this, you will need to configure npm to use your Nexus repository. You can do this by setting the `NPM_CONFIG_REGISTRY` environment variable. For example, to download your dependencies to a Nexus repository at `http://localhost:8081/repository/npm`, you would run the following command:

```
NPM_CONFIG_REGISTRY=http://localhost:8081/repository/npm npm install
```

4. **Copy your Nexus repository to your offline environment.** You can copy your Nexus repository to your offline environment using any method you like, such as using a USB drive or a network share.
5. **Configure npm to use your local Nexus repository.** To do this, set the `NPM_CONFIG_REGISTRY`environment variable to the location of your local Nexus repository. For example, if you copied your Nexus repository to `/path/to/nexus/repository/npm`, you would set the `NPM_CONFIG_REGISTRY` environment variable to `http://localhost:8081/repository/npm`.
6. **Install your dependencies in your offline environment.** You can use the `npm install`command to install your dependencies in your offline environment.
7. **Build your project.** You can use the `npm run build` command to build your project.

Here is an example of how to npm install and npm run build with Nexus npm repositories on an offline environment:

```
# Install Nexus
# Create a Nexus npm repository
# Download your dependencies to Nexus
NPM_CONFIG_REGISTRY=http://localhost:8081/repository/npm npm install

# Copy your Nexus repository to your offline environment

# Configure npm to use your local Nexus repository
NPM_CONFIG_REGISTRY=/path/to/nexus/repository/npm

# Install your dependencies in your offline environment
npm install

# Build your project
npm run build
```

**Additional notes:**

- If you are using a different shell, you will need to update your shell's configuration file to include the `NPM_CONFIG_REGISTRY` environment variable.
- You may need to run the commands above with sudo privileges.
- If you are using a private Nexus repository, you will need to authenticate to Nexus before you can download or install dependencies. You can do this by setting the `NPM_CONFIG_USERNAME` and `NPM_CONFIG_PASSWORD` environment variables.
- You can also use a Nexus proxy repository to cache dependencies from public npm repositories. This can improve performance and reduce bandwidth usage.

**Troubleshooting:**

If you are having trouble installing or running npm with Nexus npm repositories on an offline environment, here are a few things to try:

- Make sure that Nexus is running and accessible from your offline environment.
- Make sure that you have configured npm to use your local Nexus repository.
- Make sure that you have authenticated to Nexus, if required.
- Try restarting npm.
- Try searching online for help or contacting Nexus support.



