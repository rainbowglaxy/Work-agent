# Security Policy

## Maintainer

Work-agent (AgentGroupChat) is created and maintained by **Weixing Liu (刘卫星)**, GitHub account **[rainbowglaxy](https://github.com/rainbowglaxy)**. The same author name appears in this repository's `package.json` and MIT license.

As the project's maintainer, I am responsible for reviewing reported security issues, maintaining dependencies, and implementing security fixes in this application.

## Project scope

AgentGroupChat is an Electron-based desktop application for multi-model collaboration. The current version provides the desktop interface and workflow demonstrations. Live model API integration and the Codex CLI adapter are planned features.

Security review of this project focuses on Electron isolation, renderer input and output handling, external navigation, dependency risks, and credential handling when integrations are implemented.

## Reporting a vulnerability

Use this repository's private vulnerability reporting feature if it is available. Otherwise, open a GitHub issue asking the maintainer for a private reporting channel, without posting exploit details or sensitive information publicly.

A report should identify the affected version or commit, explain the issue and impact, and provide safe reproduction steps. Never include real API keys, passwords, personal information, or data belonging to others.

Testing must be limited to your own copy of this application or systems where you have explicit authorization. Third-party model providers and unrelated systems are outside the project's testing scope.

## Defensive use

I intend to use Claude for defensive security review of my own project's code, vulnerability analysis, remediation planning, and validation of fixes.
