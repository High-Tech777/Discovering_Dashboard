# Security Policy

## Supported Versions

We release patches for security vulnerabilities for the following versions:

|Version|Supported|
|-|-|
|0.1.x|:white\_check\_mark:|

## Reporting a Vulnerability

We take the security of MCP Manager seriously. If you discover a security vulnerability, please follow these steps:

### 🔒 Private Disclosure

**DO NOT** create a public GitHub issue for security vulnerabilities.

Instead, please report security vulnerabilities by:

1. **Using GitHub's Security Advisory feature**:

   * Go to the Security Advisories page
   * Click "Report a vulnerability"
   * Fill in the details
2. **Or email directly**:

   * Send an email to \[security contact - to be added]
   * Include "SECURITY" in the subject line

### 📋 What to Include

When reporting a vulnerability, please include:

* **Description**: A clear description of the vulnerability
* **Impact**: What an attacker could do with this vulnerability
* **Affected versions**: Which versions are affected
* **Steps to reproduce**: Detailed steps to reproduce the issue
* **Proof of concept**: If possible, provide a PoC
* **Suggested fix**: If you have ideas on how to fix it

### ⏱️ Response Timeline

* **Acknowledgment**: Within 48 hours
* **Initial assessment**: Within 7 days
* **Status updates**: Every 7 days until resolved
* **Fix timeline**: Varies based on severity (Critical: <7 days, High: <30 days, Medium: <90 days)

### 🏆 Recognition

We appreciate responsible disclosure. With your permission, we'll acknowledge your contribution in:

* Release notes
* Security advisories
* Project documentation

### 🛡️ Security Best Practices

When using MCP Manager:

1. **Keep Updated**: Always use the latest version
2. **Review Configurations**: Regularly audit agent configurations
3. **Limit Access**: Run with minimal required permissions
4. **Monitor Logs**: Check logs for suspicious activity
5. **Secure Deployments**: Use HTTPS in production
6. **Container Security**: Keep Docker images updated

### 🔍 Security Features

MCP Manager includes:

* **Dependency Scanning**: Automated via Dependabot
* **Code Scanning**: CodeQL analysis on every commit
* **Secure Defaults**: Safe configuration out of the box
* **Input Validation**: Strict validation of all inputs
* **Least Privilege**: Runs with minimal required permissions

### 📚 Security Resources

* [GitHub Security Best Practices](https://docs.github.com/en/code-security)
* [OWASP Top 10](https://owasp.org/www-project-top-ten/)
* [.NET Security Guidelines](https://docs.microsoft.com/en-us/dotnet/standard/security/)

Thank you for helping keep MCP Manager and its users safe! 🙏

