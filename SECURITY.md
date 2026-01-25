# Security Policy

## Supported Versions

We release patches for security vulnerabilities. Which versions are eligible for receiving such patches depends on the CVSS v3.0 Rating:

| Version | Supported          |
| ------- | ------------------ |
| latest  | :white_check_mark: |

## Reporting a Vulnerability

Please report (suspected) security vulnerabilities to **[kush.ankur0609@gmail.com](mailto:kush.ankur0609@gmail.com)**. You will receive a response from us within 48 hours. If the issue is confirmed, we will release a patch as soon as possible depending on complexity but historically within a few days.

## Security Best Practices

When using this project, please ensure you follow these security guidelines:

### API Keys and Credentials

- **Never commit real API keys** to version control
- Use environment variables or secrets management for sensitive data
- The JSON configuration files in this repository use placeholder values
- Replace `YOUR_LYZR_API_KEY_HERE` and similar placeholders with your actual credentials in a secure manner

### Knowledge Base Data

- Review all data uploaded to Knowledge Bases for sensitive information
- Do not include customer PII in sample data
- Use anonymized or synthetic data for testing and demos

### Production Deployment

- Enable HTTPS for all API communications
- Implement rate limiting to prevent abuse
- Log and monitor API access patterns
- Rotate API keys regularly
- Use least-privilege access principles

## Disclosure Policy

When we receive a security bug report, we will:

1. Confirm the problem and determine the affected versions
2. Audit code to find any potential similar problems
3. Prepare fixes for all releases still under maintenance
4. Release new security fix versions as soon as possible

## Comments on this Policy

If you have suggestions on how this process could be improved, please submit a pull request.
