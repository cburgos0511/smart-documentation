# Configure MCP Tools for Smart Documentation

> **Setting up Model Context Protocol tools for Atlassian integration**

## 🚀 Quick Setup (5 Minutes)

### Step 1: Enable MCP Tools

1. Open Cursor IDE
2. Go to Settings → Extensions
3. Search for "MCP"
4. Install the MCP Tools extension

### Step 2: Configure Atlassian MCP Server

1. Go to Settings → MCP Tools
2. Click "Add Server"
3. Select "Atlassian MCP Server"
4. Enter your Atlassian credentials

### Step 3: Test Connection

```
You: "List my Confluence spaces"
Claude: [Should show your available spaces]
```

## 📋 Detailed Configuration

### Prerequisites

- **Atlassian account** with Confluence and/or Jira access
- **API token** for your Atlassian account
- **MCP Tools extension** installed in Cursor IDE

### 1. Atlassian API Token Setup

#### Create API Token

1. Go to [Atlassian Account Settings](https://id.atlassian.com/manage-profile/security/api-tokens)
2. Click "Create API token"
3. Enter a label (e.g., "Smart Documentation Agent")
4. Copy the generated token
5. Store it securely (you won't see it again)

#### Required Permissions

Your API token needs these permissions:

- **Confluence**: Read, Write, Create pages
- **Jira**: Read issues, Create issues, Search issues
- **Atlassian ID**: Read profile information

### 2. MCP Server Configuration

#### Atlassian MCP Server Setup

1. Open Cursor IDE
2. Go to Settings → MCP Tools
3. Click "Add Server"
4. Select "Atlassian MCP Server"
5. Configure the following:

```json
{
  "name": "Atlassian MCP Server",
  "type": "atlassian",
  "config": {
    "baseUrl": "https://your-domain.atlassian.net",
    "username": "your-email@company.com",
    "apiToken": "your-api-token",
    "cloudId": "auto-detected"
  }
}
```

#### Configuration Fields

- **Base URL**: Your Atlassian instance URL
- **Username**: Your Atlassian email address
- **API Token**: The token you created
- **Cloud ID**: Will be auto-detected

### 3. Available MCP Tools

#### Confluence Tools

- `mcp_Atlassian-MCP-Server_getConfluencePage`: Read Confluence pages
- `mcp_Atlassian-MCP-Server_updateConfluencePage`: Update Confluence pages
- `mcp_Atlassian-MCP-Server_createConfluencePage`: Create new pages
- `mcp_Atlassian-MCP-Server_getConfluenceSpaces`: List available spaces
- `mcp_Atlassian-MCP-Server_searchConfluenceUsingCql`: Search Confluence content

#### Jira Tools

- `mcp_Atlassian-MCP-Server_getJiraIssue`: Read Jira issues
- `mcp_Atlassian-MCP-Server_createJiraIssue`: Create new issues
- `mcp_Atlassian-MCP-Server_searchJiraIssuesUsingJql`: Search Jira issues
- `mcp_Atlassian-MCP-Server_editJiraIssue`: Update existing issues
- `mcp_Atlassian-MCP-Server_getVisibleJiraProjects`: List accessible projects

#### User Management Tools

- `mcp_Atlassian-MCP-Server_atlassianUserInfo`: Get current user info
- `mcp_Atlassian-MCP-Server_getAccessibleAtlassianResources`: List accessible resources
- `mcp_Atlassian-MCP-Server_lookupJiraAccountId`: Look up user account IDs

### 4. Testing MCP Tools

#### Test Confluence Access

```
You: "List my Confluence spaces"
Claude: [Should show your available spaces]
```

#### Test Jira Access

```
You: "List my Jira projects"
Claude: [Should show your accessible projects]
```

#### Test Page Reading

```
You: "Read the page 'Getting Started' from Confluence"
Claude: [Should read and display the page content]
```

#### Test Page Writing

```
You: "Create a test page in Confluence called 'MCP Test'"
Claude: [Should create the page and confirm]
```

### 5. Advanced Configuration

#### Custom MCP Server Settings

```json
{
  "name": "Atlassian MCP Server",
  "type": "atlassian",
  "config": {
    "baseUrl": "https://your-domain.atlassian.net",
    "username": "your-email@company.com",
    "apiToken": "your-api-token",
    "cloudId": "auto-detected",
    "timeout": 30000,
    "retries": 3,
    "rateLimit": {
      "requests": 100,
      "window": 60000
    }
  }
}
```

#### Rate Limiting Configuration

- **Requests**: Maximum requests per window
- **Window**: Time window in milliseconds
- **Retries**: Number of retry attempts
- **Timeout**: Request timeout in milliseconds

### 6. Security Best Practices

#### API Token Security

- **Never commit** API tokens to version control
- **Use environment variables** for sensitive data
- **Rotate tokens** regularly (every 90 days)
- **Use minimal permissions** required

#### Access Control

- **Limit access** to necessary Confluence spaces
- **Use project-specific** Jira permissions
- **Monitor usage** through Atlassian audit logs
- **Revoke access** when no longer needed

## 🔧 Troubleshooting

### Common Issues

#### "Authentication failed"

- Check API token validity
- Verify username format (email address)
- Ensure token has required permissions
- Check Atlassian service status

#### "Permission denied"

- Verify Confluence space access
- Check Jira project permissions
- Ensure user has write access
- Contact Atlassian admin if needed

#### "Rate limit exceeded"

- Check rate limiting configuration
- Reduce request frequency
- Implement exponential backoff
- Contact Atlassian for higher limits

#### "Connection timeout"

- Check network connectivity
- Verify Atlassian URL format
- Increase timeout settings
- Check firewall settings

### Debugging Steps

1. **Test basic connectivity**:

   ```
   You: "Get my Atlassian user info"
   Claude: [Should return user information]
   ```

2. **Test Confluence access**:

   ```
   You: "List my Confluence spaces"
   Claude: [Should list available spaces]
   ```

3. **Test Jira access**:

   ```
   You: "List my Jira projects"
   Claude: [Should list accessible projects]
   ```

4. **Test specific operations**:
   ```
   You: "Read page 'Test' from space 'DOC'"
   Claude: [Should read the page content]
   ```

## ✅ Verification Checklist

### Basic Connectivity

- [ ] MCP Tools extension installed
- [ ] Atlassian MCP Server configured
- [ ] API token valid and working
- [ ] Can get user information

### Confluence Access

- [ ] Can list Confluence spaces
- [ ] Can read existing pages
- [ ] Can create new pages
- [ ] Can update existing pages

### Jira Access

- [ ] Can list Jira projects
- [ ] Can read Jira issues
- [ ] Can create Jira issues
- [ ] Can search Jira issues

### Advanced Features

- [ ] Can search Confluence content
- [ ] Can manage Jira workflows
- [ ] Can handle rate limiting
- [ ] Can process large responses

## 🎯 Next Steps

### Ready for Production

Once MCP tools are configured and tested:

- [Create your Smart Documentation Agent](create-agent-config.md)
- [Set up team workflows](team-adoption.md)
- [Configure advanced features](advanced-configuration.md)

### Testing Your Setup

1. **Basic test**: Ask Claude to list your Confluence spaces
2. **Read test**: Ask Claude to read a Confluence page
3. **Write test**: Ask Claude to create a test page
4. **Full test**: Ask Claude to update documentation

---

**TL;DR:** Install MCP Tools extension, configure Atlassian MCP Server with your API token, test Confluence and Jira access, and verify all tools are working. This gives Claude direct access to your Atlassian ecosystem for automated documentation management.
