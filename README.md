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

### **2. Prerequisites – Install Node.js and npm

To begin, install **Node.js** and **npm** (Node Package Manager). npm is included automatically when installing Node.js.

```
# Update package lists
sudo apt update

# Install Node.js and npm
sudo apt install nodejs npm -y

# Verify installation
node -v
npm -v
```

---

### **3. Install the Gemini CLI**

Use **npm** to install the Gemini CLI tool globally. The `-g` flag ensures the `gemini` command is available from any directory.

```
sudo npm install -g @google/gemini-cli
```

---

### **4. Link Your Google Account (Authentication)**

Authenticate the CLI to your Google account using:

```
gemini auth login
```

This will open a browser or provide a URL where you can sign in and authorize the CLI. This allows the tool to identify your account and determine which models you can access under the free tier.


---

### **5. Verify the Installation**

Test your setup by running a sample prompt:

```
gemini "What is the purpose of a command-line interface?"
```

If everything is working correctly, you will receive a response from Gemini directly in your terminal.

---

