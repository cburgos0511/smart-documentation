# Setup Guide: Cursor IDE with Claude Integration

> **Step-by-Step Setup for Smart Documentation Agent**

## 🚀 Quick Setup (10 Minutes)

### Step 1: Download and Install Cursor IDE

1. Go to [cursor.sh](https://cursor.sh/)
2. Download for your operating system
3. Run the installer
4. Launch Cursor IDE

### Step 2: Enable Claude Integration

1. Open Cursor IDE
2. Go to Settings → Extensions
3. Search for "Claude"
4. Install and enable the Claude extension

### Step 3: Configure API Access

1. Go to Settings → Claude
2. Enter your Claude API key
3. Test the connection

### Step 4: Test the System

```
You: "Hello Claude, can you help me with documentation?"
Claude: [Should respond with helpful documentation assistance]
```

## 📋 Detailed Setup Instructions

### Prerequisites

- **Operating System**: Windows 10+, macOS 10.15+, or Linux
- **Memory**: 8GB RAM minimum, 16GB recommended
- **Storage**: 2GB free space
- **Internet**: Stable connection for AI integration

### 1. Cursor IDE Installation

#### Windows

```bash
# Download from https://cursor.sh/
# Run the installer as administrator
# Follow the installation wizard
```

#### macOS

```bash
# Download from https://cursor.sh/
# Open the .dmg file
# Drag Cursor to Applications folder
# Launch from Applications
```

#### Linux

```bash
# Download from https://cursor.sh/
# Extract the archive
# Run the installation script
sudo ./install.sh
```

### 2. Claude Integration Setup

#### Enable Claude Extension

1. Open Cursor IDE
2. Press `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (macOS)
3. Search for "Claude"
4. Click "Install" on the Claude extension
5. Restart Cursor IDE

#### Configure Claude Settings

1. Go to File → Preferences → Settings
2. Search for "Claude"
3. Configure the following settings:
   - **API Key**: Enter your Claude API key
   - **Model**: Select "claude-3-sonnet" (recommended)
   - **Temperature**: Set to 0.7 (balanced creativity)
   - **Max Tokens**: Set to 4000 (for comprehensive responses)

#### Test Claude Integration

1. Open a new file in Cursor IDE
2. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
3. Type "Claude: Chat"
4. Start a conversation with Claude

### 3. MCP Tools Configuration

#### Enable MCP Tools

1. Go to Settings → Extensions
2. Search for "MCP"
3. Install the MCP Tools extension
4. Restart Cursor IDE

#### Configure Atlassian MCP Server

1. Go to Settings → MCP Tools
2. Click "Add Server"
3. Select "Atlassian MCP Server"
4. Enter your Atlassian credentials:
   - **Atlassian URL**: Your Confluence/Jira URL
   - **Username**: Your Atlassian username
   - **API Token**: Your Atlassian API token

#### Test MCP Connection

```
You: "List my Confluence spaces"
Claude: [Should show your available Confluence spaces]
```

### 4. Agent Configuration

#### Create Agent Directory

```bash
# Create the agent configuration directory
mkdir -p .claude/agents
```

#### Create Smart Documentation Agent

Create `.claude/agents/smart-documentation-agent.md`:

```markdown
# Smart Documentation Agent

## Purpose

Automatically generate and maintain comprehensive documentation using AI analysis of codebase and direct Confluence integration.

## Capabilities

- Analyze codebase structure and patterns
- Generate PSM-format documentation
- Update Confluence pages directly
- Maintain bidirectional references
- Create Jira issues for documentation tasks

## Documentation Format

Use PSM (Product Support Management) format with sections:

- PSM (Support Team)
- Key User Concepts
- Potential Questions
- Technical Implementation

## MCP Tools to Use

- mcp_Atlassian-MCP-Server_getConfluencePage
- mcp_Atlassian-MCP-Server_updateConfluencePage
- mcp_Atlassian-MCP-Server_createJiraIssue
- Filesystem tools for local file management

## Workflow

1. Analyze codebase for documentation needs
2. Generate comprehensive documentation
3. Update Confluence pages via MCP tools
4. Update local documentation files
5. Maintain bidirectional references
6. Create Jira issues for follow-up tasks
```

## 🔧 Troubleshooting

### Common Issues

#### "Claude not responding"

- Check API key configuration
- Verify internet connection
- Restart Cursor IDE
- Check Claude service status

#### "MCP tools not working"

- Verify MCP extension is installed
- Check Atlassian credentials
- Test API token validity
- Restart Cursor IDE

#### "Agent not found"

- Check agent file location (`.claude/agents/`)
- Verify file format (markdown)
- Check file permissions
- Restart Cursor IDE

### Getting Help

1. **Check Cursor IDE logs**: View → Output → Claude
2. **Test individual components**: Test Claude and MCP separately
3. **Verify credentials**: Check API keys and tokens
4. **Restart services**: Restart Cursor IDE and try again

## ✅ Verification Checklist

### Claude Integration

- [ ] Claude extension installed and enabled
- [ ] API key configured correctly
- [ ] Claude responds to test queries
- [ ] Claude can read and write files

### MCP Tools

- [ ] MCP extension installed and enabled
- [ ] Atlassian MCP Server configured
- [ ] Atlassian credentials working
- [ ] Can access Confluence spaces
- [ ] Can access Jira projects

### Agent Configuration

- [ ] Agent directory created (`.claude/agents/`)
- [ ] Smart Documentation Agent file created
- [ ] Agent file format is correct
- [ ] Agent is recognized by Claude

### System Integration

- [ ] Claude can use MCP tools
- [ ] File system access working
- [ ] Confluence integration working
- [ ] Jira integration working

## 🎯 Next Steps

### Test the System

1. **Basic test**: Ask Claude to read a file
2. **MCP test**: Ask Claude to list Confluence spaces
3. **Agent test**: Ask Claude to analyze your codebase
4. **Full test**: Ask Claude to update documentation

### Ready for Production

Once all tests pass, you're ready to:

- [Create your first documentation update](create-agent-config.md)
- [Set up team workflows](team-adoption.md)
- [Configure advanced features](advanced-configuration.md)

---

**TL;DR:** Download Cursor IDE, install Claude extension, configure MCP tools with Atlassian credentials, create agent config file, and test the system. The entire setup takes about 10 minutes and gives you a fully functional Smart Documentation Agent.
