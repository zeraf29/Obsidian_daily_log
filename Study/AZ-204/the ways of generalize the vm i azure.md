

--- 
author: zeraf29
created: 2023-11-17 08:46 
last-updated: 2023-11-17 08:46 
summaries: 
tags:

---


## Memo


Here are the ways to generalize a VM in Azure:

- **Sysprep:** Sysprep is a tool that prepares a Windows VM for generalized deployment. It removes machine-specific information from the VM, making it possible to clone the VM and deploy it to multiple machines.
- **Generalize and Capture:** Generalize and Capture is a feature of the Azure portal that allows you to capture a generalized image of a VM. This image can then be used to deploy new VMs.
- **PowerShell:** You can use PowerShell to generalize a VM. This method is more complex than using sysprep or Generalize and Capture, but it gives you more control over the generalization process.

Here are the steps on how to generalize a VM in Azure using sysprep:

1. Sign in to the VM.
2. Open a Command Prompt window as an administrator.
3. Run the following command:

```
sysprep /generalize /shutdown
```

4. The VM will shut down.
5. Once the VM has shut down, you can create a generalized image of the VM using the Azure portal or PowerShell.

Here are the steps on how to generalize a VM in Azure using Generalize and Capture:

1. Sign in to the Azure portal.
2. Navigate to the VM that you want to generalize.
3. In the Overview blade, click the **Generalize and capture** button.
4. In the Generalize and capture blade, select the **Generalize** option.
5. Click the **Capture** button.
6. Azure will create a generalized image of the VM.

Here are the steps on how to generalize a VM in Azure using PowerShell:

1. Sign in to your Azure subscription using PowerShell.
2. Run the following command to get the VM object:

```
Get-AzureRMVM -ResourceGroupName <resource_group_name> -VMName <vm_name>
```

3. Run the following command to generalize the VM:

```
Set-AzureRMVMGeneralizedImage -VM <vm_object>
```

4. Run the following command to capture a generalized image of the VM:

```
New-AzureRMVMImage -ResourceGroupName <resource_group_name> -VMName <vm_name>
```

5. Azure will create a generalized image of the VM.

Once you have generalized a VM, you can deploy it to multiple machines. To deploy a generalized VM, you can use the Azure portal, PowerShell, or the Azure CLI.

Here are the steps on how to deploy a generalized VM using the Azure portal:

1. Sign in to the Azure portal.
2. Navigate to the **VM Images** blade.
3. Click the **Create** button.
4. Select the **Generalized** image option.
5. Select the generalized image that you want to deploy.
6. Click the **Create** button.
7. Azure will deploy the VM to the specified resource group and region.

Here are the steps on how to deploy a generalized VM using PowerShell:

1. Sign in to your Azure subscription using PowerShell.
2. Run the following command to create a new VM configuration object:

```
New-AzureRMVMConfig -VMName <vm_name> -VMSize <vm_size>
```

3. Run the following command to set the VM image to the generalized image that you want to deploy:

```
$config.VMImage = Get-AzureRMVMImage -ResourceGroupName <resource_group_name> -Name <image_name>
```

4. Run the following command to deploy the VM:

```
New-AzureRMVM -ResourceGroupName <resource_group_name> -VMName <vm_name> -VM -VMConfig $config
```

5. Azure will deploy the VM to the specified resource group and region.

Here are the steps on how to deploy a generalized VM using the Azure CLI:

1. Sign in to your Azure subscription using the Azure CLI.
2. Run the following command to create a new resource group:

```
az group create --name <resource_group_name>
```

3. Run the following command to deploy the VM:

az vm create --resource-group <resource_group_name> --name <vm_name> --image <image_name> --size <vm_size>

4. Azure will deploy the VM to the specified resource group and region.




|Method|Pros|Cons|
|---|---|---|
|Sysprep|Simple, easy to use|Can be time-consuming, requires shutting down the VM|
|Generalize and Capture|Fast, easy to use|Less control over the generalization process|
|PowerShell|Flexible, gives you more control over the generalization process|More complex, requires some PowerShell knowledge|

Sheets로 내보내기

In general, I recommend using Generalize and Capture for most VMs. It is a fast and easy-to-use method that does not require shutting down the VM. However, if you need more control over the generalization process, then you can use sysprep or PowerShell.

Here is a table that summarizes the key differences between the three methods:

|Feature|Sysprep|Generalize and Capture|PowerShell|
|---|---|---|---|
|Requires shutting down the VM|Yes|No|No|
|Requires PowerShell knowledge|No|No|Yes|
|Gives you control over the generalization process|Limited|Limited|Full|
|Ease of use|Easy|Easy|Moderate|
|Speed|Slow|Fast|Moderate|

Sheets로 내보내기
