---
title: "Creating a Virtual Machine and Installing the Web Server Role in Windows Server"
datePublished: Fri Sep 01 2023 22:56:13 GMT+0000 (Coordinated Universal Time)
cuid: clm18xux5005z74nva50de8l1
slug: creating-a-virtual-machine-and-installing-the-web-server-role-in-windows-server

---

In today's digital age, the ability to set up and manage virtual machines is a crucial skill for IT professionals. In this guide, we will walk you through the process of creating a virtual machine and installing the web server role on Microsoft Windows Server.

### **Step 1: Sign in to Azure Portal**

1.1. Open your web browser and navigate to the Azure portal at [https://portal.azure.com](https://portal.azure.com).

1.2. Sign in with your Azure account credentials. If you don't have an Azure account, you can create one following the on-screen instructions.

### **Step 2: Create a Virtual Machine**

2.1. Once you're logged in, click on the "+ Create a resource" button in the left-hand menu.

2.2. In the Azure Marketplace search bar, type "Windows Server" and press Enter.

2.3. Choose a Windows Server version from the search results. Typically, Windows Server 2019 is a good choice.

2.4. Click the "Create" button to begin configuring your virtual machine.

### **Step 3: Configure Virtual Machine Settings**

3.1. Fill out the basic settings for your virtual machine:

   - **Project details**: Select your subscription, resource group, and region.

   - **Instance details**: Give your VM a unique name and choose an availability option. For testing purposes, you can select "No infrastructure redundancy required."

   - **Image**: Choose the Windows Server image you selected earlier.

   - **Size**: Select an appropriate size for your VM based on your performance and cost requirements.

3.2. In the "Administrator account" section, set a username and a strong password. This will be your login information for the VM.

3.3. Leave other settings as their default values for now, or customize them as needed.

3.4. Click the "Review + create" button to review your settings and then click "Create" to create the virtual machine.

### **Step 4: Connect to the Virtual Machine**

4.1. Once the VM is deployed, go to the VM's overview page.

4.2. Under "Settings," click on "Connect."

4.3. Download the Remote Desktop Protocol (RDP) file to connect to your VM.

4.4. Open the RDP file and enter the username and password you set during VM configuration.

### **Step 5: Install Web Server Role**

5.1. Once connected to your VM, open the "Server Manager" by clicking on the Windows icon in the taskbar and selecting "Server Manager."

5.2. In Server Manager, click on "Add roles and features."

5.3. Follow the wizard to add the "Web Server (IIS)" role.

5.4. Complete the installation by accepting the default role services or customizing them as needed.

5.5. Once installed, you can access the default IIS web page by opening a web browser and entering the VM's IP address or DNS name.

Congratulations! You've successfully created a virtual machine in Azure and installed the web server role on Windows Server. You can now start hosting and managing web applications on your VM.