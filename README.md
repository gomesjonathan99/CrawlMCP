# MCP-Agent-Hub

A comprehensive collection of Model Context Protocol (MCP) servers featuring custom FireCrawl integration and community-contributed MCP servers from the @openbnb ecosystem.

## 🚀 Overview

MCP-Agent-Hub serves as a centralized repository for various MCP servers that enable AI agents to interact with external tools and services. This hub includes:

- **Custom FireCrawl MCP Server**: Web scraping and content extraction capabilities
- **@openbnb Community MCPs**: Curated collection of community-contributed MCP servers
- **Ready-to-use configurations**: Pre-configured setups for popular AI clients

## 🔧 What is MCP?

The Model Context Protocol (MCP) is an open standard that enables AI assistants to securely access external data sources and tools. MCP servers act as bridges between AI models and various services, allowing for enhanced functionality and real-world integration.

## 📦 Available MCP Servers

### FireCrawl MCP Server
- **Purpose**: Web scraping and content extraction
- **Features**: 
  - Website crawling and data extraction
  - Content parsing and structuring
  - Rate limiting and ethical scraping practices
  - Support for various content formats

### @openbnb Community MCPs
A collection of community-contributed MCP servers providing various functionalities such as:
- Database integrations
- API connectors
- File system operations
- External service integrations

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- Node.js (for certain MCP servers)
- Git

### Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/devgomesai/MCP-Agent-Hub.git
   cd MCP-Agent-Hub
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure your MCP client:**
   Add the MCP servers to your client configuration (Claude Desktop, Continue, etc.)

## ⚙️ Configuration

### Claude Desktop Configuration

Add the following to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "python",
      "args": ["path/to/firecrawl-mcp/server.py"],
      "env": {
        "FIRECRAWL_API_KEY": "your_api_key_here"
      }
    }
  }
}
```

### Environment Variables

Create a `.env` file with necessary API keys and configurations:

```env
FIRECRAWL_API_KEY=your_firecrawl_api_key
# Add other API keys as needed
```

## 🎯 Usage Examples

### Using FireCrawl MCP

```python
# Example usage through MCP
# The AI assistant can now scrape websites and extract content
"Please scrape the homepage of example.com and summarize the main content"
```

### Community MCP Servers

Each community MCP server comes with its own usage instructions and examples. Check the individual server directories for specific documentation.

## 🤝 Contributing

We welcome contributions to expand the MCP-Agent-Hub! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b feature/new-mcp-server`
3. **Add your MCP server** with proper documentation
4. **Test your implementation**
5. **Submit a pull request**

### Contribution Guidelines

- Ensure your MCP server follows the official MCP specification
- Include comprehensive documentation and examples
- Add appropriate error handling and logging
- Test with common MCP clients (Claude Desktop, Continue, etc.)
- Follow the established directory structure

## 📁 Project Structure

```
MCP-Agent-Hub/
├── firecrawl-mcp/          # Custom FireCrawl MCP server
│   ├── server.py
│   ├── requirements.txt
│   └── README.md
├── community-mcps/         # @openbnb community MCPs
│   ├── server1/
│   ├── server2/
│   └── ...
├── examples/              # Usage examples and configurations
├── docs/                  # Documentation
├── tests/                 # Test files
├── requirements.txt       # Main dependencies
└── README.md             # This file
```

## 🔧 Troubleshooting

### Common Issues

1. **MCP Server Not Connecting**
   - Verify your configuration file syntax
   - Check that all required dependencies are installed
   - Ensure API keys are correctly set in environment variables

2. **Permission Errors**
   - Make sure Python scripts have execute permissions
   - Verify file paths in configuration

3. **API Rate Limits**
   - Check your API key limits
   - Implement proper rate limiting in custom servers

### Debug Mode

Enable debug logging by setting the environment variable:
```bash
export MCP_DEBUG=true
```

## 📚 Documentation

- [MCP Specification](https://github.com/modelcontextprotocol/specification)
- [Claude Desktop MCP Guide](https://docs.anthropic.com/claude/docs/mcp)
- [FireCrawl API Documentation](https://docs.firecrawl.dev/)

## 🛡️ Security & Best Practices

- **API Key Management**: Never commit API keys to version control
- **Rate Limiting**: Implement appropriate rate limiting for external APIs
- **Error Handling**: Provide robust error handling and meaningful error messages
- **Logging**: Implement proper logging for debugging and monitoring
- **Validation**: Validate all inputs and outputs

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [@openbnb](https://github.com/openbnb) community for MCP server contributions
- [Anthropic](https://anthropic.com) for the Model Context Protocol specification
- [FireCrawl](https://firecrawl.dev) for web scraping capabilities
- All contributors who have helped expand this hub

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/devgomesai/mcp-nexus/issues)
- **Discussions**: [GitHub Discussions](https://github.com/devgomesai/mcp-nexus/discussions)
- **Documentation**: Check the `/docs` directory for detailed guides

---

**Note**: This is a community-driven project. Please ensure you comply with the terms of service of any external APIs or services used through these MCP servers.
