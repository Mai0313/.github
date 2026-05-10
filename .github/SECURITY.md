# Security Policy

The security of the projects under this account is taken seriously. This document outlines the policy for reporting and handling security vulnerabilities. We appreciate the efforts of security researchers and the broader community in helping keep these projects and their users safe.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

If you believe you have identified a security vulnerability, please report it through one of the following private channels:

1. **GitHub Security Advisories** (preferred)
   Use the **"Report a vulnerability"** button under the **Security** tab of the affected repository. This opens a private advisory visible only to the maintainers.

2. **Email**
   Send a report to **<mai@mai0313.com>** with the subject prefix `[SECURITY]` followed by the repository name. PGP-encrypted email is welcome upon request.

You should receive an acknowledgement within the timelines listed below. If you do not, please follow up to ensure the original message was received.

### What to Include in a Report

To help us triage and resolve the issue efficiently, please include as much of the following as possible:

- A clear description of the vulnerability and its potential impact
- The affected repository, version, commit hash, or release tag
- Step-by-step instructions to reproduce the issue
- Proof-of-concept code, exploit scripts, or screenshots (if available)
- Any known mitigations or suggested remediations
- Whether the vulnerability has been disclosed elsewhere
- Your name or handle and how you would like to be credited (optional)

Reports written in **English** are preferred to avoid translation ambiguity.

## Response and Disclosure Process

Once a report is received, the following process will be followed:

| Stage | Target Timeline |
| --- | --- |
| Initial acknowledgement of the report | Within **48 hours** |
| Initial triage and severity assessment | Within **7 days** |
| Status update during investigation | At least every **14 days** |
| Fix, mitigation, or formal response | Depends on severity and complexity |
| Public disclosure after fix is released | Coordinated with the reporter |

We follow a **coordinated disclosure** model:

1. The report is acknowledged and triaged privately.
2. A fix or mitigation is developed and validated.
3. A new release is published containing the fix.
4. A security advisory is published, crediting the reporter unless anonymity is requested.
5. CVE identifiers will be requested when applicable.

We kindly ask that reporters refrain from disclosing the vulnerability publicly until a fix has been released and the advisory has been published.

## Severity Classification

Severity is assessed using a CVSS v3.1-aligned approach:

- **Critical** — Remote code execution, authentication bypass, or large-scale data exposure
- **High** — Privilege escalation, sensitive data leakage, or significant integrity issues
- **Medium** — Limited information disclosure, denial-of-service, or weakened security controls
- **Low** — Minor issues with limited real-world impact

Response priority and release cadence are calibrated to the assessed severity.

## Scope

### In Scope

- Source code in repositories under this account
- Build, packaging, and release artifacts published from these repositories
- Continuous integration and deployment workflows defined in the repositories
- Documentation that, if incorrect, could lead to insecure usage

### Out of Scope

- Vulnerabilities in third-party dependencies (please report these to the upstream project; if exploitable through this project, a report is still welcome)
- Issues requiring physical access to a user's device or unrealistic threat models
- Social engineering, phishing, or attacks against maintainers or users
- Reports generated solely by automated scanners without demonstrated impact
- Best-practice recommendations without an associated, demonstrable security impact
- Denial-of-service issues caused by excessive resource consumption that require unrealistic input sizes

## Safe Harbor

We support **good-faith security research**. If you make a sincere effort to comply with this policy, we will:

- Consider your research to be authorized under this policy
- Work with you to understand and resolve the issue promptly
- Not pursue or support legal action related to your research

In return, we ask that you:

- Avoid privacy violations, destruction of data, and disruption of services
- Use only test accounts or your own data when validating an issue
- Provide a reasonable amount of time to remediate before any public disclosure
- Do not exploit the vulnerability beyond what is necessary to demonstrate it

## Supported Versions

Unless explicitly stated otherwise in a specific repository, only the **latest released version** receives active security maintenance. Older versions may receive fixes on a best-effort basis.

| Version | Supported |
| --- | --- |
| Latest release | ✅ |
| Older releases | ❌ (best-effort only) |

## Security Practices

The repositories under this account adopt the following baseline security practices:

- **Dependency monitoring** via [Dependabot](https://github.com/dependabot) for automated vulnerability alerts and updates
- **Secret scanning** using [Gitleaks](https://github.com/gitleaks/gitleaks) to prevent accidental credential leaks
- **Pre-commit hooks** that enforce linting, formatting, and security checks before code reaches the repository
- **Branch protection** requiring code review and passing CI checks before merging
- **Pinned actions and reproducible builds** in CI workflows where applicable
- **Principle of least privilege** for tokens and workflow permissions

## Acknowledgements

We are grateful to the researchers and contributors who responsibly disclose security issues. With the reporter's permission, we will publicly acknowledge contributions in the relevant security advisory or release notes.

## Policy Updates

This policy may be updated periodically to reflect evolving practices and project requirements. Material changes will be reflected in the repository history of this file.
