# ☁️ Cloud-Powered Portfolio Deployment Guide

Welcome to the comprehensive guide for deploying an impressive front-end portfolio website using Azure Cloud services.

## Prerequisites 📋

Before initiating the deployment, ensure you have the following:

-  An active Azure account with sufficient permissions to create resources.
-  Fundamental understanding of Azure services.
-  Your portfolio website's HTML and CSS files.

## 🛠️ Steps to Deploy

### 1. Virtual Network (VNet) Creation

Begin by creating a Virtual Network (VNet) in the Azure portal:

1. Sign in to the Azure portal.
2. Go to "Create a resource" > "Networking" > "Virtual Network".
3. Configure the VNet settings to align with your requirements.

### 2. Virtual Machine (VM) Deployment

Deploy two Virtual Machines within the VNet:

1. Navigate to "Create a resource" > "Compute" > "Virtual Machine".
2. Configure each VM to be located within the previously created VNet.

### 3. File Share Setup

Create a File Share to securely store your website files:

1. Visit "Storage accounts" and create a new storage account.
2. Generate a File Share inside the storage account.

### 4. Mounting File Share to VMs

Mount the created File Share to the deployed VMs:

1. Access each VM via Remote Desktop Protocol (RDP).
2. Map the File Share using the Azure Storage Account credentials.

### 5. Path of HTML and CSS Files on File Share

Identify and note the path of your HTML and CSS files within the mounted File Share to configure the web server later.

### 6. Installation of Internet Information Services (IIS) on VMs

Install IIS on both VMs to serve your website:

1. Connect to each VM via Remote Desktop Protocol (RDP).
2. Utilize Server Manager to add the IIS role.
3. Configure IIS to point to the HTML and CSS files' path on the mounted File Share.

### 7. Load Balancer Configuration

Set up a Load Balancer to evenly distribute traffic:

1. In the Azure portal, navigate to "Create a resource" > "Networking" > "Load Balancer".
2. Follow the prompts to create a Load Balancer and configure the backend pool with both VMs.

### 8. DNS Zone and Public IP Assignment

Associate a public IP with the Load Balancer and configure the DNS zone:

1. Assign a public IP to the Load Balancer.
2. Configure an A record in your DNS provider to link to the public IP of the Load Balancer.

## 🚀 Congratulations

You have successfully launched your front-end portfolio website using Azure Cloud services,
Your website is now live and accessible through the assigned DNS.

## Contact Us 📧

Have questions, feedback, or need assistance? feel free to contact:

- Email: [hrushikeshdagwar@gmail.com](mailto:hrushikeshdagwar@gmail.com)
