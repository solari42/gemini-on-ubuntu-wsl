# gemini-on-ubuntu-wsl
Gemini CLI is the GOAT, It's better than the web versions. I think this particular model is specifically for building, and I've tested it. It's powerful enough to help me out as a beginner.

# WSL Installation and Setup Guide

## Introduction

This guide documents my journey and the steps I followed to install and configure Windows Subsystem for Linux (WSL) on my Windows machine. WSL allows me to run a Linux environment directly within Windows, which is incredibly useful for development, testing, and learning Linux tools.

---

## Installation Steps

### **1. Enable WSL and Virtual Machine Platform**

To begin, I enabled the necessary Windows features by opening **PowerShell as Administrator** and running the following commands:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

After running these commands, a system restart may be required.

---

### **2. Install the WSL Update Package**

I downloaded and installed the latest **WSL2 Linux kernel update package** from Microsoft's official documentation to ensure compatibility and performance improvements.

---

### **3. Set WSL 2 as the Default Version**

To ensure that all newly installed Linux distributions use WSL 2 by default, I ran:

```
wsl --set-default-version 2
```

---

### **4. Install a Linux Distribution (Ubuntu)**

I selected **Ubuntu** and downloaded it from the Microsoft Store. Upon launching it for the first time, I created my Linux username and password.

---

### **5. Initial Ubuntu Configuration**

After installing Ubuntu, I updated system packages and installed essential developer tools:

```
sudo apt update
sudo apt upgrade -y
sudo apt install build-essential git -y
```

---

## What I Learned / Key Takeaways

* WSL provides a seamless bridge between Windows and Linux environments.
* Understanding the difference between **WSL 1** and **WSL 2** helped me optimize performance.
* The `wsl` command is powerful for managing Linux distributions on Windows.
* Examples of potential learnings to add:

  * Navigating between Windows and Linux filesystems.
  * Setting up VS Code integration with WSL.
  * Fixing common WSL-related errors.

---

## Future Notes / Troubleshooting

* **[Document any issues encountered and their solutions]**
* **[List further configurations planned]**
* **[Include links to helpful resources such as Microsoft Docs or tutorials]**

---

*This guide is part of my ongoing learning journey as I continue to explore Linux, development workflows, and system configuration.*

## Installing a Gemini CLI on WSL (Ubuntu)

This guide covers how to install a community-developed Command-Line Interface (CLI) for interacting with Google’s Gemini models directly from the Ubuntu terminal.

---

### **1. Prerequisites: Update Ubuntu and Install Pip**

First, ensure your system is up to date and that you have **pip**, the Python package installer.

```
# Update package lists and upgrade existing packages
sudo apt update && sudo apt upgrade -y

# Install pip
sudo apt install python3-pip -y
```

---

### **2. Isolate the Installation (Optional but Recommended)**

To keep your system clean, use **pipx**, which installs Python CLI tools in isolated environments.

```
# Install pipx
sudo apt install pipx -y

# Make sure pipx is added to your PATH
pipx ensurepath
```

> You may need to restart your terminal after this step for the PATH changes to take effect.

---

### **3. Install the Gemini CLI Tool**

Use `pipx` (or `pip` if you skipped Step 2) to install a community-made Gemini CLI tool, such as **gemini-cli**.

```
pipx install gemini-cli
```

---

### **4. Configure the CLI with Your API Key**

You need an API key to authenticate with Google's Gemini API.

1. Visit **Google AI Studio** and generate an API key.
2. Run the configuration command:

```
gemini configure
```

Enter your API key when prompted. The CLI will store it securely.

---

### **5. Verify the Installation**

Test your setup by running a sample prompt:

```
gemini "What is the purpose of a command-line interface?"
```

If everything is working correctly, you will receive a response from Gemini directly in your terminal.

---

