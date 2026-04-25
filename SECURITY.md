# Security Policy ✦

> *MiladyAI takes the security of our elizaOS agents, APIs, and infrastructure seriously. We appreciate responsible disclosure.*

---

## Supported Versions

| Repository | Supported Versions |
|:-----------|:-------------------|
| `core` | Latest stable release |
| `api` | Latest stable release |
| `sdk` | Latest stable release |
| elizaOS plugins (`plugin-*`) | Latest stable release |
| Character files | All versions |

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, email us at: **security@miladyai.xyz**

Include in your report:
- Description of the vulnerability
- Affected repository and version
- Steps to reproduce
- Potential impact
- Any suggested fixes (optional)

We will acknowledge your report within **48 hours** and provide a detailed response within **7 days** explaining our assessment and next steps.

---

## elizaOS-Specific Security Considerations

Since MiladyAI agents run on the [elizaOS](https://github.com/elizaOS/eliza) runtime, please also consider these elizaOS-specific vectors when reporting:

- **Prompt injection** in elizaOS agent Actions or Providers
- **Plugin sandbox escapes** — elizaOS plugins running with elevated permissions
- **Character file manipulation** — malicious `lore` or `knowledge` injections
- **elizaOS client token leakage** — Twitter/Discord/Telegram API keys in logs or error messages
- **elizaOS memory (RAG) poisoning** — injecting malicious content into agent knowledge bases
- **Multi-agent trust boundaries** — elizaOS agent-to-agent communication attacks

If the vulnerability is in elizaOS core itself (not MiladyAI code), please also report it to [elizaOS security](https://github.com/elizaOS/eliza/security).

---

## Disclosure Policy

- We follow a **90-day responsible disclosure** timeline
- We will credit reporters in our release notes (unless anonymity is requested)
- We do not pursue legal action against good-faith security researchers
- Coordinated disclosure is always preferred over immediate public disclosure

---

## Bug Bounty

We do not currently have a formal bug bounty program, but we deeply appreciate security researchers who help keep MiladyAI and the elizaOS ecosystem safe. Significant findings may be rewarded at maintainer discretion.

---

<div align="center">
<sub>MiladyAI · Powered by <a href="https://github.com/elizaOS/eliza">elizaOS</a> · Report vulnerabilities to security@miladyai.xyz</sub>
</div>
