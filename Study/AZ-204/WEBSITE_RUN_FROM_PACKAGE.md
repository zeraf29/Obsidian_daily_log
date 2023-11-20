

--- 
author: zeraf29
created: 2023-11-21 08:35 
last-updated: 2023-11-21 08:35 
summaries: 
tags:

---


## Memo

The WEBSITE_RUN_FROM_PACKAGE app setting in Azure App Service allows you to run your web application directly from a deployment package file, rather than deploying the application files to the App Service instance's file system. This can be useful for a few reasons:

- **Reduced deployment time:** The deployment process is faster because the package file is transferred to the App Service instance and extracted directly into the application's runtime environment, rather than having to copy all of the application files individually.
    
- **Reduced disk usage:** The application files are stored in the deployment package file, rather than on the App Service instance's file system. This can be useful for applications that have large amounts of static content.
    
- **Simplified deployment process:** The deployment process is simplified because you do not need to worry about copying or updating the application files on the App Service instance. You simply need to upload the deployment package file to the App Service instance's storage account.
    

To enable WEBSITE_RUN_FROM_PACKAGE, you can set the app setting to "1" in the Azure portal, the Azure CLI, or Azure PowerShell.

Here are some additional things to keep in mind when using WEBSITE_RUN_FROM_PACKAGE:

- The maximum size of the deployment package file is 1 GB.
- The deployment package file must be a ZIP file.
- The deployment package file must contain all of the application files that the application needs to run.
- The application files must be extracted to the correct location in the deployment package file.

Overall, WEBSITE_RUN_FROM_PACKAGE is a useful feature that can simplify the deployment process and reduce deployment time for web applications that are deployed to Azure App Service.


