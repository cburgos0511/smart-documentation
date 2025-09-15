# Create Smart Documentation Agent Configuration

> **Setting up your AI agent for automated documentation management**

## 🚀 Quick Setup (5 Minutes)

### Step 1: Create Agent Directory

```bash
mkdir -p .claude/agents
```

### Step 2: Create Agent Configuration

Create `.claude/agents/smart-documentation-agent.md` with the template below

### Step 3: Test Agent

```
You: "Analyze our codebase and create documentation"
Claude: [Should use the agent configuration]
```

## 📋 Detailed Configuration

### Prerequisites

- **Cursor IDE** with Claude integration
- **MCP Tools** configured with Atlassian access
- **Agent directory** created (`.claude/agents/`)

### 1. Basic Agent Configuration

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
- mcp_Atlassian-MCP-Server_createConfluencePage
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

### 2. Advanced Agent Configuration

For more sophisticated setups, use this enhanced configuration:

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
- Handle multiple documentation formats
- Support team-specific workflows

## Documentation Format

Use PSM (Product Support Management) format with sections:

- PSM (Support Team)
- Key User Concepts
- Potential Questions
- Technical Implementation

## MCP Tools to Use

- mcp_Atlassian-MCP-Server_getConfluencePage
- mcp_Atlassian-MCP-Server_updateConfluencePage
- mcp_Atlassian-MCP-Server_createConfluencePage
- mcp_Atlassian-MCP-Server_createJiraIssue
- mcp_Atlassian-MCP-Server_searchJiraIssuesUsingJql
- Filesystem tools for local file management

## Workflow

1. Analyze codebase for documentation needs
2. Generate comprehensive documentation
3. Update Confluence pages via MCP tools
4. Update local documentation files
5. Maintain bidirectional references
6. Create Jira issues for follow-up tasks

## Configuration

- **Default Space**: DOC (Confluence space for documentation)
- **Default Project**: DOC (Jira project for documentation tasks)
- **File Location**: ./docs/ (local documentation directory)
- **Format**: Markdown with PSM structure
- **References**: Bidirectional between local and Confluence

## Quality Standards

- **Accuracy**: Documentation must match actual code
- **Completeness**: All features must be documented
- **Consistency**: Standardized format across all docs
- **Currency**: Documentation must be up-to-date
- **Clarity**: Clear explanations for all audiences

## Error Handling

- **Graceful failures**: Continue with partial updates
- **Detailed logging**: Log all operations and errors
- **User notification**: Inform user of any issues
- **Rollback capability**: Ability to revert changes

## Team Integration

- **Collaborative editing**: Support multiple contributors
- **Version control**: Track changes and history
- **Review process**: Support for documentation reviews
- **Approval workflow**: Require approval for major changes
```

### 3. Team-Specific Configurations

#### For Enterprise Teams

```markdown
# Smart Documentation Agent - Enterprise Configuration

## Purpose

Enterprise-grade documentation automation with compliance and governance.

## Additional Capabilities

- Compliance reporting
- Audit trail maintenance
- Multi-team coordination
- Enterprise security standards

## Configuration

- **Compliance**: SOX, GDPR, HIPAA as applicable
- **Audit**: Complete operation logging
- **Security**: Enterprise-grade access controls
- **Governance**: Approval workflows for changes

## Quality Standards

- **Compliance**: Meet all regulatory requirements
- **Security**: Follow enterprise security policies
- **Governance**: Adhere to corporate standards
- **Audit**: Maintain complete audit trail
```

#### For Consulting Firms

```markdown
# Smart Documentation Agent - Consulting Configuration

## Purpose

Client-focused documentation automation for project delivery.

## Additional Capabilities

- Client-specific formatting
- Project-based organization
- Handoff documentation
- Client approval workflows

## Configuration

- **Client Format**: Customizable for each client
- **Project Structure**: Organized by project
- **Handoff Process**: Automated client delivery
- **Approval**: Client review and approval

## Quality Standards

- **Client Satisfaction**: Meet client expectations
- **Professional**: High-quality presentation
- **Complete**: Comprehensive project documentation
- **Timely**: Deliver on schedule
```

#### For Open Source Projects

```markdown
# Smart Documentation Agent - Open Source Configuration

## Purpose

Community-focused documentation automation for open source projects.

## Additional Capabilities

- Contributor-friendly format
- Community guidelines
- Translation support
- Accessibility standards

## Configuration

- **Community**: Contributor-friendly documentation
- **Accessibility**: WCAG 2.1 AA compliance
- **Translation**: Multi-language support
- **Guidelines**: Community contribution standards

## Quality Standards

- **Accessibility**: Accessible to all users
- **Inclusive**: Welcoming to new contributors
- **Comprehensive**: Complete project documentation
- **Maintainable**: Easy to keep current
```

### 4. Customization Options

#### Documentation Format Customization

```markdown
## Custom Documentation Format

- **Sections**: Customize section structure
- **Templates**: Use project-specific templates
- **Styling**: Custom CSS and formatting
- **Metadata**: Additional metadata fields
```

#### Workflow Customization

```markdown
## Custom Workflow

- **Triggers**: Custom trigger conditions
- **Actions**: Custom action sequences
- **Approvals**: Custom approval processes
- **Notifications**: Custom notification rules
```

#### Integration Customization

```markdown
## Custom Integrations

- **Additional Tools**: Custom MCP tools
- **APIs**: Custom API integrations
- **Webhooks**: Custom webhook endpoints
- **Automation**: Custom automation rules
```

### 5. Testing Your Configuration

#### Basic Test

```
You: "Test the Smart Documentation Agent"
Claude: [Should use the agent configuration]
```

#### Functionality Test

```
You: "Analyze our codebase and create documentation"
Claude: [Should follow the configured workflow]
```

#### Integration Test

```
You: "Update our Confluence documentation"
Claude: [Should use MCP tools as configured]
```

#### Full Test

```
You: "Create comprehensive documentation for our project"
Claude: [Should execute the complete workflow]
```

## 🔧 Troubleshooting

### Common Issues

#### "Agent not found"

- Check file location (`.claude/agents/`)
- Verify file format (markdown)
- Check file permissions
- Restart Cursor IDE

#### "Configuration error"

- Check markdown syntax
- Verify all required sections
- Check for typos in tool names
- Validate configuration format

#### "MCP tools not working"

- Verify MCP tools are configured
- Check Atlassian credentials
- Test MCP tools separately
- Restart Cursor IDE

#### "Workflow not following"

- Check workflow configuration
- Verify tool availability
- Check error messages
- Test individual steps

### Debugging Steps

1. **Check agent file**:

   - Verify file exists in `.claude/agents/`
   - Check markdown format
   - Validate configuration syntax

2. **Test MCP tools**:

   - Test Confluence access
   - Test Jira access
   - Verify tool permissions

3. **Test workflow**:

   - Test individual steps
   - Check error messages
   - Verify tool availability

4. **Check logs**:
   - View Cursor IDE logs
   - Check Claude responses
   - Verify MCP tool responses

## ✅ Verification Checklist

### Agent Configuration

- [ ] Agent file created in `.claude/agents/`
- [ ] Markdown format is correct
- [ ] All required sections present
- [ ] Configuration syntax is valid

### MCP Integration

- [ ] MCP tools are configured
- [ ] Atlassian credentials working
- [ ] Tools are accessible to agent
- [ ] Error handling is configured

### Workflow Testing

- [ ] Basic agent test passes
- [ ] Functionality test passes
- [ ] Integration test passes
- [ ] Full workflow test passes

### Team Integration

- [ ] Team-specific configuration applied
- [ ] Quality standards defined
- [ ] Error handling configured
- [ ] Workflow is documented

## 🎯 Next Steps

### Ready for Production

Once your agent is configured and tested:

- [Set up team workflows](team-adoption.md)
- [Configure advanced features](advanced-configuration.md)
- [Start documenting your project](getting-started.md)

### Customization

- **Team-specific**: Customize for your team's needs
- **Project-specific**: Adapt for your project requirements
- **Process-specific**: Align with your development process
- **Tool-specific**: Integrate with your existing tools

---

**TL;DR:** Create `.claude/agents/smart-documentation-agent.md` with your agent configuration, customize for your team's needs, test the configuration, and verify all components are working. This gives you a fully configured AI agent for automated documentation management.
