# Contributing to Lyzr Customer Support Agents

First off, thank you for considering contributing! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Pull Request Process](#pull-request-process)
- [Style Guidelines](#style-guidelines)
- [Community](#community)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear title** describing the issue
- **Steps to reproduce** the behavior
- **Expected behavior** vs what actually happened
- **Screenshots** if applicable
- **Environment details** (Lyzr Studio version, browser, etc.)

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please include:

- **Use case** - Why is this enhancement needed?
- **Proposed solution** - How should it work?
- **Alternatives considered** - Other approaches you've thought about

### 🔧 Pull Requests

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit with clear messages (`git commit -m 'Add amazing feature'`)
5. Push to your branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## Getting Started

### Prerequisites

- [Lyzr Studio Account](https://studio.lyzr.ai/)
- Basic understanding of AI agents and JSON configuration
- Familiarity with Git and GitHub

### Local Development

1. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/lyzr-customer-support-agents.git
   cd lyzr-customer-support-agents
   ```

2. Create a branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make changes and test in Lyzr Studio

4. Commit and push your changes

## Pull Request Process

1. **Update documentation** if you change agent configurations
2. **Update CHANGELOG.md** with your changes
3. **Ensure no sensitive data** (API keys, credentials) is committed
4. **Request review** from maintainers
5. **Address feedback** promptly

### PR Checklist

- [ ] I have read the contributing guidelines
- [ ] My code follows the project's style guidelines
- [ ] I have updated the documentation accordingly
- [ ] I have added/updated tests if applicable
- [ ] All API keys and sensitive data are placeholder values
- [ ] I have updated CHANGELOG.md

## Style Guidelines

### JSON Configuration Files

- Use 2-space indentation
- Keep agent instructions well-formatted with clear sections
- Use descriptive names for agents and fields
- Always use placeholder values for sensitive data:
  - `"api_key": "YOUR_LYZR_API_KEY_HERE"`
  - `"rag_id": "YOUR_RAG_ID_HERE"`

### Documentation

- Use clear, concise language
- Include code examples where helpful
- Keep README.md up to date with any changes
- Use proper Markdown formatting

### Commit Messages

Follow conventional commits:
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation only
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Maintenance tasks

Examples:
```
feat: Add escalation handling to manager agent
fix: Correct KB citation format in policy assistant
docs: Update setup guide with troubleshooting section
```

## Community

- **Questions?** Open a [Discussion](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/discussions)
- **Found a bug?** Open an [Issue](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/issues)
- **Want to contribute?** Submit a [Pull Request](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/pulls)

## Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes when their changes are included

---

Thank you for helping make this project better! 🙏
