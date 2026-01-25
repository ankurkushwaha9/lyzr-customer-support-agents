# Contributing to Lyzr Customer Support Agents

First off, thank you for considering contributing to this project! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Pull Request Process](#pull-request-process)
- [Style Guidelines](#style-guidelines)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## How Can I Contribute?

### 🐛 Reporting Bugs

- Ensure the bug was not already reported by searching on GitHub under [Issues](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/issues)
- If you're unable to find an open issue addressing the problem, [open a new one](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/issues/new)
- Include a clear title and description
- Provide as much relevant information as possible
- Include code samples or agent configurations if applicable

### 💡 Suggesting Enhancements

- Open a new issue with the `enhancement` label
- Provide a clear description of the proposed feature
- Explain why this enhancement would be useful
- Include examples of how the feature would work

### 🔧 Pull Requests

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Getting Started

### Prerequisites

- [Lyzr Studio Account](https://studio.lyzr.ai/)
- Basic understanding of AI agents and multi-agent systems
- Familiarity with JSON configuration files

### Local Setup

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/lyzr-customer-support-agents.git
   cd lyzr-customer-support-agents
   ```
3. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Pull Request Process

1. **Update Documentation**: If you're adding new agents or modifying existing ones, update the relevant documentation in the `docs/` folder and README.md.

2. **Follow JSON Standards**: Ensure all agent JSON files are properly formatted and validated.

3. **Sanitize Credentials**: Never commit real API keys or sensitive data. Use placeholders like:
   - `YOUR_LYZR_API_KEY_HERE`
   - `YOUR_RAG_ID_HERE`
   - `YOUR_AGENT_ID_HERE`

4. **Test Your Changes**: If possible, test your agent configurations in Lyzr Studio before submitting.

5. **Describe Your Changes**: Write a clear PR description explaining:
   - What changes were made
   - Why the changes were necessary
   - How to test the changes

6. **Link Related Issues**: Reference any related issues using `Fixes #123` or `Closes #123`.

## Style Guidelines

### JSON Files

- Use 2-space indentation
- Keep agent instructions clear and well-organized
- Use descriptive names for agents and fields
- Include comments in documentation (not in JSON)

### Documentation

- Use clear, concise language
- Include code examples where helpful
- Keep formatting consistent with existing docs
- Use Markdown properly

### Commit Messages

Follow conventional commit format:
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation changes
- `refactor:` for code refactoring
- `test:` for adding tests

Examples:
```
feat: Add new escalation agent for complex queries
fix: Correct KB retrieval parameters in policy agent
docs: Update setup guide with troubleshooting section
```

## Reporting Bugs

When reporting bugs, please include:

1. **Description**: A clear and concise description of the bug
2. **Steps to Reproduce**: 
   - Step 1
   - Step 2
   - ...
3. **Expected Behavior**: What you expected to happen
4. **Actual Behavior**: What actually happened
5. **Environment**:
   - Lyzr Studio version (if known)
   - Browser (if applicable)
   - Any relevant configuration
6. **Screenshots**: If applicable, add screenshots

## Suggesting Enhancements

When suggesting enhancements, please include:

1. **Use Case**: Describe the problem or use case
2. **Proposed Solution**: How you envision the enhancement working
3. **Alternatives Considered**: Any alternative solutions you've thought about
4. **Additional Context**: Any other information that might be helpful

## Questions?

Feel free to open an issue with the `question` label if you have any questions about contributing.

---

Thank you for contributing! 🙏
