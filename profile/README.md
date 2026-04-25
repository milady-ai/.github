<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=24&height=200&section=header&text=MiladyAI&fontSize=80&fontColor=fff&animation=fadeIn&fontAlignY=38&desc=Aesthetic%20AI%20Agents%20on%20elizaOS&descAlignY=55&descSize=20" width="100%"/>

<p>
  <img src="https://img.shields.io/badge/Powered%20by-elizaOS-blueviolet?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0tMiAxNWwtNS01IDEuNDEtMS40MUwxMCAxNC4xN2w3LjU5LTcuNTlMMTkgOGwtOSA5eiIvPjwvc3ZnPg==&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/elizaOS-Agents-ff69b4?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-0075ca?style=for-the-badge"/>
</p>

</div>

---

## ✦ What is MiladyAI?

**MiladyAI** is an open-source AI agent organization building at the intersection of **culture**, **creativity**, and **autonomous intelligence**. Our agents are fully deployed on **[elizaOS](https://github.com/elizaOS/eliza)** — the leading open-source multi-agent AI framework.

We believe the future of AI is **agentic, aesthetic, and open**. Every agent we ship runs on elizaOS and is available for the community to fork, remix, and extend.

---

## ✦ Built on elizaOS

All MiladyAI agents run on the **[elizaOS](https://github.com/elizaOS/eliza)** runtime. elizaOS is a powerful, modular framework for building autonomous AI agents that operate across social platforms, APIs, and on-chain environments.

```
elizaOS runtime
├── AgentRuntime          ← orchestrates everything
├── Character Files       ← agent persona & config (.json)
├── Plugins               ← modular capabilities
│   ├── Actions           ← what the agent does
│   ├── Providers         ← context fed into the agent
│   └── Evaluators        ← how the agent scores outputs
├── Clients               ← Twitter, Discord, Telegram, ...
└── Memory (RAG)          ← vector-based long-term memory
```

> 📖 [elizaOS docs](https://eliza.how) · [elizaOS GitHub](https://github.com/elizaOS/eliza) · [elizaOS Discord](https://discord.gg/elizaos)

---

## ✦ Our elizaOS Agents & Projects

| Repository | elizaOS Role | Description |
|:-----------|:-------------|:------------|
| 🌸 **milady-agent** | elizaOS character + plugins | The flagship MiladyAI social agent |
| 🔌 **plugin-aesthetic** | elizaOS Action/Provider | Aesthetic scoring & image ranking |
| 🎭 **characters** | elizaOS character files | All MiladyAI agent persona configs |
| 🧠 **knowledge** | elizaOS RAG/memory | Curated knowledge bases for agents |
| 🔮 **plugin-onchain** | elizaOS Action | On-chain interactions via elizaOS |
| 📡 **plugin-feeds** | elizaOS Provider | Real-time context injection |
| 📦 **sdk** | TypeScript/Python | SDK wrapping elizaOS for MiladyAI |
| 📚 **docs** | — | Documentation and guides |

---

## ✦ elizaOS Plugin Architecture

MiladyAI extends elizaOS through a suite of purpose-built plugins. Here's the core plugin pattern we follow:

```typescript
import { Plugin } from "@elizaos/core";

export const miladyPlugin: Plugin = {
  name: "milady-core",
  description: "Core MiladyAI capabilities for elizaOS agents",
  actions: [/* elizaOS Actions */],
  providers: [/* elizaOS Providers */],
  evaluators: [/* elizaOS Evaluators */],
};
```

Our elizaOS character files wire everything together:

```json
{
  "name": "Milady",
  "modelProvider": "anthropic",
  "clients": ["twitter", "discord", "telegram"],
  "plugins": [
    "@miladyai/plugin-aesthetic",
    "@miladyai/plugin-onchain",
    "@elizaos/plugin-bootstrap",
    "@elizaos/plugin-image-generation"
  ]
}
```

---

## ✦ Tech Stack

<div align="center">

![elizaOS](https://img.shields.io/badge/elizaOS-framework-blueviolet?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

</div>

---

## ✦ Get Involved

Whether you're an elizaOS contributor, an AI researcher, or just an aesthetic enjoyer:

1. 🔌 **Build** a new elizaOS plugin for MiladyAI agents
2. 🎭 **Remix** a character file and propose it via PR
3. 🐛 **Fix** bugs — check issues tagged `good first issue`
4. 📖 **Read** our [Contributing Guide](../CONTRIBUTING.md) to understand the elizaOS plugin workflow
5. 💬 **Join** the conversation on Discord or GitHub Discussions

> *"The most beautiful machine is the one that understands you."*

---

## ✦ elizaOS Resources

<div align="center">

[![elizaOS GitHub](https://img.shields.io/badge/elizaOS%20GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/elizaOS/eliza)
[![elizaOS Docs](https://img.shields.io/badge/elizaOS%20Docs-0075ca?style=for-the-badge&logo=gitbook&logoColor=white)](https://eliza.how)
[![elizaOS Discord](https://img.shields.io/badge/elizaOS%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/elizaos)

</div>

---

## ✦ MiladyAI Community

<div align="center">

[![Twitter/X](https://img.shields.io/badge/Twitter%2FX-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/miladyai)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/miladyai)
[![Website](https://img.shields.io/badge/Website-FF69B4?style=for-the-badge&logo=vercel&logoColor=white)](https://miladyai.xyz)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/miladyai)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=24&height=100&section=footer" width="100%"/>

<sub>MiladyAI · Built on <a href="https://github.com/elizaOS/eliza">elizaOS</a> · Made with 🌸 by the community · <a href="https://github.com/milady-ai">github.com/milady-ai</a></sub>

</div>
