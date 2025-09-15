# Getting Started with Smart Documentation Agent

> **From Zero to Perfect Documentation in 30 Minutes**

## 🚀 Quick Start (5 Minutes)

### Step 1: Install Cursor IDE

1. Download [Cursor IDE](https://cursor.sh/)
2. Install the Claude integration
3. Sign in with your account

### Step 2: Configure MCP Tools

1. Open Cursor settings
2. Navigate to MCP tools section
3. Enable Atlassian MCP Server
4. Connect your Atlassian account

### Step 3: Test the System

```
You: "Analyze our codebase and create documentation for our main features"
Claude: [Does all the work automatically]
```

## 📋 Prerequisites

### Required

- **Cursor IDE** with Claude integration
- **Atlassian account** (Confluence access)
- **Codebase** to document

### Optional

- **Jira access** for task management
- **Git repository** for version control
- **Team workspace** for collaboration

## 🛠️ Detailed Setup

### 1. Cursor IDE Configuration

#### Install Cursor IDE

```bash
# Download from https://cursor.sh/
# Follow installation instructions for your OS
```

#### Enable Claude Integration

1. Open Cursor IDE
2. Go to Settings → Extensions
3. Search for "Claude"
4. Install and enable

#### Configure API Access

1. Go to Settings → Claude
2. Enter your API key
3. Test connection

### 2. MCP Atlassian Setup

#### Enable MCP Tools

1. Open Cursor settings
2. Navigate to "MCP Tools"
3. Enable "Atlassian MCP Server"

#### Connect Atlassian Account

1. Click "Connect Atlassian"
2. Sign in with your Atlassian credentials
3. Authorize Cursor to access your workspace

#### Test Connection

```
You: "List my Confluence spaces"
Claude: [Shows your available spaces]
```

### 3. Create Agent Configuration

#### Create Agent File

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
```

## 🎯 Your First Documentation Update

### Example 1: Update Existing Documentation

```
You: "Update the documentation for our user authentication system"

Claude will:
1. Read your authentication-related code files
2. Analyze the current implementation
3. Generate comprehensive documentation
4. Update the corresponding Confluence page
5. Update your local documentation file
6. Maintain all references
```

### Example 2: Create New Documentation

```
You: "Create documentation for our new payment processing feature"

Claude will:
1. Analyze the payment processing code
2. Understand the architecture and data flow
3. Generate PSM-format documentation
4. Create a new Confluence page
5. Create a local documentation file
6. Set up bidirectional references
```

### Example 3: Bulk Documentation Update

```
You: "Update all our feature documentation to match our new PSM format"

Claude will:
1. Scan your entire documentation directory
2. Read all existing documentation files
3. Analyze the current format
4. Update all files to PSM format
5. Update all corresponding Confluence pages
6. Ensure perfect consistency
```

## 🔧 Troubleshooting

### Common Issues

#### "Claude can't access my Confluence"

- Check MCP Atlassian connection
- Verify Atlassian permissions
- Test with a simple query first

#### "Documentation format is inconsistent"

- Check agent configuration file
- Ensure PSM format is specified
- Review generated content

#### "Local files not updating"

- Check file permissions
- Verify agent has filesystem access
- Test with a simple file read/write

### Getting Help

1. **Check the FAQ**: [community/FAQ.md](../community/FAQ.md)
2. **Review examples**: [examples/](../examples/)
3. **Test with simple queries**: Start with basic requests
4. **Check logs**: Review Cursor IDE logs for errors

## 🎉 Success Indicators

### You'll Know It's Working When:

- Claude can read your Confluence pages
- Documentation updates happen automatically
- Local and remote files stay in sync
- New team members can understand your codebase quickly

### Next Steps

- [Team Adoption Guide](../guides/team-adoption.md)
- [Advanced Configuration](../guides/create-agent-config.md)
- [Business Case](../business-case.md)

---

**TL;DR:** Install Cursor IDE, enable MCP Atlassian tools, create agent config, then just talk to Claude to update your documentation. The system handles everything automatically - code analysis, documentation generation, Confluence updates, and local file sync.
