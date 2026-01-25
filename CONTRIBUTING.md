# Contributing to Lyzr Customer Support Agents

First off, thank you for considering contributing to this project! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Pull Request Process](#pull-request-process)
- [Style Guidelines](#style-guidelines)
- [Community](#community)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [kush.ankur0609@gmail.com](mailto:kush.ankur0609@gmail.com).

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (agent configurations, API calls, etc.)
- **Describe the behavior you observed and what you expected**
- **Include screenshots** if applicable
- **Include your environment details** (Lyzr Studio version, browser, etc.)

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please include:

- **Use a clear and descriptive title**
- **Provide a detailed description** of the suggested enhancement
- **Explain why this enhancement would be useful**
- **List any alternative solutions** you've considered

### 🔧 Contributing Code

#### Types of contributions we're looking for:

- New agent configurations for different use cases
- Improvements to existing agent instructions
- Documentation improvements
- Bug fixes
- New features

## Getting Started

1. **Fork the repository** on GitHub

2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/lyzr-customer-support-agents.git
   cd lyzr-customer-support-agents
   ```

3. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

4. **Make your changes** and test them in Lyzr Studio

5. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add: brief description of your changes"
   ```

6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Open a Pull Request** from your fork to the main repository

## Pull Request Process

1. **Ensure your PR description clearly describes the problem and solution**
2. **Include the relevant issue number** if applicable
3. **Update documentation** if you're changing functionality
4. **Ensure all agent JSON files are valid** and properly formatted
5. **Remove any sensitive data** (API keys, personal information) before submitting
6. **Wait for review** - maintainers will review your PR and may request changes

### PR Title Convention

Use these prefixes for PR titles:
- `Add:` for new features or agents
- `Fix:` for bug fixes
- `Update:` for updates to existing functionality
- `Docs:` for documentation changes
- `Refactor:` for code refactoring

## Style Guidelines

### Agent Configuration Files

- Use **valid JSON** format with proper indentation (2 spaces)
- **Sanitize all sensitive data** before committing:
  - Replace API keys with `YOUR_LYZR_API_KEY_HERE`
  - Replace RAG IDs with `YOUR_*_RAG_ID`
  - Replace Agent IDs with `YOUR_*_AGENT_ID`
- Include **clear descriptions** for agents
- Write **comprehensive instructions** for agent behavior

### Documentation

- Use **clear, concise language**
- Include **code examples** where helpful
- Keep **formatting consistent** with existing docs
- Update the **Table of Contents** if adding new sections

### Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

## Community

### Getting Help

- **GitHub Issues** - For bugs and feature requests
- **GitHub Discussions** - For questions and general discussion
- **Lyzr Documentation** - [docs.lyzr.ai](https://docs.lyzr.ai/)
- **Lyzr Community** - [Lyzr Discord/Slack]

### Recognition

Contributors will be recognized in the following ways:
- Listed in the Contributors section of the README
- Mentioned in release notes for significant contributions

---

## Thank You! 🙏

Your contributions help make this project better for everyone. We appreciate your time and effort!

---

*This contributing guide is adapted from open-source best practices and the [Contributor Covenant](https://www.contributor-covenant.org/).*
