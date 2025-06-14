# MCP Setup: Connect VS Code (Server) with Cursor (Client)

This project demonstrates how to connect two different editors — **Visual Studio Code** and **Cursor** — using **MCP (Model-Connected Programming)** to allow code execution, debugging, and interaction across both tools.

---

## Goal

To use:

- **VS Code** as the **MCP server** (where the code runs)  
- **Cursor** as the **MCP client** (where the code is edited and AI-assisted)

---

## Project Structure
GEN-AI/
└── genai-cohort/
└── mcp-weather/
└── index.js


This `index.js` is the entry point for your Node.js server that gets run by MCP.

---

## How I Set It Up

1. **Opened VS Code** — this acted as the MCP **server**.  
2. **Opened Cursor** — this acted as the MCP **client**.  
3. Inside Cursor, I opened the **MCP Tool** and added this configuration:

```json
{
  "mcpServers": {
    "weather-server": {
      "command": "node",
      "args": ["./GEN-AI/genai-cohort/mcp-weather/index.js"],
      "env": {
        "API_KEY": "your_actual_api_key_here"
      }
    }
  }
}

 


