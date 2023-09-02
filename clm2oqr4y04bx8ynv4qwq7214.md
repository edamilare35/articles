---
title: "🚀 How to Recall SSH and RDP Ports for Instance Maintenance After a 🌩️ Failure"
datePublished: Sat Sep 02 2023 21:19:26 GMT+0000 (Coordinated Universal Time)
cuid: clm2oqr4y04bx8ynv4qwq7214
slug: how-to-recall-ssh-and-rdp-ports-for-instance-maintenance-after-a-failure
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693699146517/2b1a252f-14ac-442e-8501-1d943147cef0.jpeg

---


Introduction:

Maintaining and troubleshooting computing instances is a critical task for system administrators and IT professionals. Occasionally, unforeseen failures or issues may require you to recall the SSH (Secure Shell) and RDP (Remote Desktop Protocol) ports to access an instance for maintenance and recovery. In this article, we will outline a comprehensive guide on how to recall these ports to connect to the instance effectively. 🛠️

## Step 1: Access Instance Information

Before recalling the SSH and RDP ports, you need to gather essential information about the instance. This includes:

- **Instance Name or IP Address**: Identify the specific instance you are targeting. 🏢

- **Instance Operating System**: Know whether it is a Linux or Windows instance, as SSH and RDP are platform-specific protocols. 🐧🪟

## Step 2: Check Documentation 📚

If you have well-maintained documentation for your instances, refer to it first. Documentation should contain details such as port numbers, credentials, and any specific configuration instructions. Check for any recent updates or changes that may have been made before the failure occurred. 📝

## Step 3: Review Configuration Files 📂

### Recalling SSH Port (Linux):

For Linux-based instances, SSH is commonly used. To recall the SSH port:

- Log in to the instance if possible using any known methods.
- Navigate to the SSH configuration file. It's typically located at `/etc/ssh/sshd_config`.
- Open the configuration file using a text editor like `nano` or `vim`.
- Look for the "Port" directive. This specifies the SSH port number. For example, "Port 22" is the default. 🔒

### Recalling RDP Port (Windows):

For Windows-based instances, RDP is used. To recall the RDP port:

- If you can access the instance, open "Server Manager."
- Go to "Local Server" and check the "Remote Desktop" section. The RDP port number should be displayed there. 🪟

## Step 4: Check Network Scanning Tools 🌐

If you cannot access the instance due to the failure, you can use network scanning tools like `nmap` or `Advanced IP Scanner`. Scan the instance's IP address to identify open ports. Be sure to respect security policies and firewalls. 🛡️

Example command for `nmap`:

```bash
nmap -p 1-65535 <instance_IP>
```

## Step 5: Contact Support or Administrator ☎️

If you are unable to find the port information using the above methods, reach out to your system administrator or support team. They may have the necessary information or can guide you through the recovery process. 🆘

## Step 6: Port Forwarding (if necessary) ↗️

If the instance is behind a firewall or NAT (Network Address Translation), you may need to set up port forwarding rules on the network device to allow SSH or RDP traffic to reach the instance. Consult your network administrator or documentation for this step. 🌐🔌

## Conclusion 🌟

Recalling SSH and RDP ports is a crucial step when you need to access an instance for maintenance after a failure. It involves checking documentation, configuration files, network scanning tools, and contacting support when necessary. Proper preparation and documentation can significantly streamline this process, ensuring a faster response to critical issues and minimizing downtime. 🚀🛠️