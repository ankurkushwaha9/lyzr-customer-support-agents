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

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear title** describing the issue
- **Steps to reproduce** the behavior
- **Expected behavior** vs actual behavior
- **Screenshots** if applicable
- **Environment details** (Lyzr Studio version, browser, OS)

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please include:

- **Clear title** for the suggestion
- **Detailed description** of the proposed feature
- **Use case** explaining why this would be useful
- **Examples** of how it would work

### 🔧 Contributing Code

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## Getting Started

### Prerequisites

- [Lyzr Studio Account](https://studio.lyzr.ai/)
- Basic understanding of AI agents and multi-agent systems
- Familiarity with JSON configuration

### Local Development

1. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/lyzr-customer-support-agents.git
   cd lyzr-customer-support-agents
   ```

2. Create a branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes and test them in Lyzr Studio

4. Commit and push your changes

## Pull Request Process

1. **Update documentation** if you're changing agent configurations or adding features
2. **Test your changes** in Lyzr Studio before submitting
3. **Fill out the PR template** completely
4. **Link related issues** using keywords like "Fixes #123"
5. **Request review** from maintainers
6. **Address feedback** promptly

### PR Checklist

- [ ] I have read the contributing guidelines
- [ ] My code follows the project's style guidelines
- [ ] I have tested my changes in Lyzr Studio
- [ ] I have updated documentation as needed
- [ ] I have added comments for complex logic
- [ ] All API keys and sensitive data are replaced with placeholders

## Style Guidelines

### JSON Configuration Files

- Use 2-space indentation
- Keep descriptions clear and concise
- Always use placeholder values for sensitive data:
  - `"api_key": "YOUR_LYZR_API_KEY_HERE"`
  - `"rag_id": "YOUR_RAG_ID_HERE"`

### Documentation

- Use clear, concise language
- Include code examples where helpful
- Keep README sections organized
- Use proper Markdown formatting

### Commit Messages

Follow conventional commits format:

```
type(scope): description

[optional body]

[optional footer]
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Formatting changes
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

Examples:
```
feat(agents): add escalation handling to manager agent
fix(docs): correct API endpoint in setup guide
docs(readme): add architecture diagram
```

## Community

### Getting Help

- **GitHub Issues**: For bugs and feature requests
- **Discussions**: For questions and general discussion
- **Lyzr Discord**: Join the [Lyzr community](https://discord.gg/lyzr)

### Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes for significant contributions

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).

---

Thank you for contributing! 🚀
