# gemini-on-ubuntu-wsl
Gemini CLI is the GOAT, It's better than the web versions. I think this particular model is specifically for building, and I've tested it. It's powerful enough to help me out as a beginner.

---

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

