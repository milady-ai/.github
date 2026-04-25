<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=000000&height=240&section=header&text=MiladyAI&fontSize=100&fontColor=D4AF37&animation=fadeIn&fontAlignY=42&desc=Aesthetic%20AI%20Agents%20on%20elizaOS&descAlignY=58&descSize=22&descColor=D4AF37" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=Cinzel&size=26&duration=3000&pause=600&color=D4AF37&center=true&vCenter=true&width=720&lines=Aesthetic+AI+Agents+%E2%9C%A6+Black+%26+Gold;Built+on+elizaOS+%E2%80%94+Powered+by+Culture" alt="typing" />

<p>
<img src="https://img.shields.io/badge/Powered%20by-elizaOS-FF6B35?style=for-the-badge&labelColor=000000"/>
<img src="https://img.shields.io/badge/Status-Active-D4AF37?style=for-the-badge&labelColor=000000"/>
<img src="https://img.shields.io/badge/elizaOS-Agents-FF6B35?style=for-the-badge&labelColor=000000"/>
<img src="https://img.shields.io/badge/License-MIT-D4AF37?style=for-the-badge&labelColor=000000"/>
</p>

</div>

---

## ✦ What is MiladyAI?

**MiladyAI** is an open-source AI agent organization building at the intersection of **culture**, **creativity**, and **autonomous intelligence**. Our agents are fully deployed on [![elizaOS](https://img.shields.io/badge/elizaOS-FF6B35?style=flat-square&labelColor=000000)](https://github.com/elizaOS/eliza) — the leading open-source multi-agent AI framework.

We believe the future of AI is **agentic, aesthetic, and open**. Every agent we ship runs on elizaOS and is available for the community to fork, remix, and extend.

---

## ✦ Built on elizaOS

All MiladyAI agents run on the [![elizaOS](https://img.shields.io/badge/elizaOS-FF6B35?style=flat-square&labelColor=000000)](https://github.com/elizaOS/eliza) runtime. elizaOS is a powerful, modular framework for building autonomous AI agents that operate across social platforms, APIs, and on-chain environments.

```
elizaOS runtime
├── AgentRuntime         ← orchestrates everything
├── Character Files      ← agent persona & config (.json)
├── Plugins              ← modular capabilities
│   ├── Actions          ← what the agent does
│   ├── Providers        ← context fed into the agent
│   └── Evaluators       ← how the agent scores outputs
├── Clients              ← Twitter, Discord, Telegram, ...
└── Memory (RAG)         ← vector-based long-term memory
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

![elizaOS](https://img.shields.io/badge/elizaOS-framework-FF6B35?style=flat-square&labelColor=000000)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white&labelColor=000000)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white&labelColor=000000)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white&labelColor=000000)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white&labelColor=000000)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white&labelColor=000000)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-D4AF37?style=flat-square&logo=githubactions&logoColor=black&labelColor=000000)

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

## ✦ Contributors

<div align="center">

<a href="https://github.com/odilitime"><img src="https://github.com/odilitime.png" width="80" height="80" alt="odilitime"/></a>
<a href="https://github.com/lalalune"><img src="https://github.com/lalalune.png" width="80" height="80" alt="lalalune"/></a>
<a href="https://github.com/HaruHunab1320"><img src="https://github.com/HaruHunab1320.png" width="80" height="80" alt="HaruHunab1320"/></a>
<a href="https://github.com/Dexploarer"><img src="https://github.com/Dexploarer.png" width="80" height="80" alt="Dexploarer"/></a>
<a href="https://github.com/0xSolace"><img src="https://github.com/0xSolace.png" width="80" height="80" alt="0xSolace"/></a>
<a href="https://github.com/2-A-M"><img src="https://github.com/2-A-M.png" width="80" height="80" alt="2-A-M"/></a>
<a href="https://github.com/binkyfishai"><img src="https://github.com/binkyfishai.png" width="80" height="80" alt="binkyfishai"/></a>
<a href="https://github.com/dutchiono"><img src="https://github.com/dutchiono.png" width="80" height="80" alt="dutchiono"/></a>
<a href="https://github.com/HomunculusLabs"><img src="https://github.com/HomunculusLabs.png" width="80" height="80" alt="HomunculusLabs"/></a>
<a href="https://github.com/mavisakalyan"><img src="https://github.com/mavisakalyan.png" width="80" height="80" alt="mavisakalyan"/></a>
<a href="https://github.com/NubsCarson"><img src="https://github.com/NubsCarson.png" width="80" height="80" alt="NubsCarson"/></a>
<a href="https://github.com/wakesync"><img src="https://github.com/wakesync.png" width="80" height="80" alt="wakesync"/></a>
<a href="https://github.com/Ziflie"><img src="https://github.com/Ziflie.png" width="80" height="80" alt="Ziflie"/></a>

</div>

---

## ✦ elizaOS Resources

<div align="center">

[![elizaOS GitHub](https://img.shields.io/badge/elizaOS%20GitHub-FF6B35?style=for-the-badge&logo=github&logoColor=white&labelColor=000000)](https://github.com/elizaOS/eliza)
[![elizaOS Docs](https://img.shields.io/badge/elizaOS%20Docs-FF6B35?style=for-the-badge&logo=gitbook&logoColor=white&labelColor=000000)](https://eliza.how)
[![elizaOS Discord](https://img.shields.io/badge/elizaOS%20Discord-FF6B35?style=for-the-badge&logo=discord&logoColor=white&labelColor=000000)](https://discord.gg/elizaos)

</div>

---

## ✦ MiladyAI Community

<div align="center">

[![Twitter/X](https://img.shields.io/badge/Twitter%2FX-D4AF37?style=for-the-badge&logo=x&logoColor=black&labelColor=000000)](https://x.com/miladyai)
[![Discord](https://img.shields.io/badge/Discord-D4AF37?style=for-the-badge&logo=discord&logoColor=black&labelColor=000000)](https://discord.gg/miladyai)
[![Website](https://img.shields.io/badge/Website-D4AF37?style=for-the-badge&logo=vercel&logoColor=black&labelColor=000000)](https://miladyai.xyz)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-D4AF37?style=for-the-badge&logo=huggingface&logoColor=black&labelColor=000000)](https://huggingface.co/miladyai)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=000000&height=100&section=footer" width="100%"/>

<sub>MiladyAI · Built on <a href="https://github.com/elizaOS/eliza">elizaOS</a> · Made with 🌸 by the community · <a href="https://github.com/milady-ai">github.com/milady-ai</a></sub>

</div>
