# Contributing to MiladyAI ✦

> *MiladyAI is built on [elizaOS](https://github.com/elizaOS/eliza) — the open-source AI agent framework powering autonomous agents across the ecosystem. Every contribution here extends elizaOS.*

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [elizaOS Architecture Overview](#elizaos-architecture-overview)
- [Getting Started](#getting-started)
- [Building elizaOS Plugins for MiladyAI](#building-elizaos-plugins-for-miladyai)
- [Character Files](#character-files)
- [Pull Request Process](#pull-request-process)
- [Commit Convention](#commit-convention)

---

## Code of Conduct

All contributors must follow our [Code of Conduct](CODE_OF_CONDUCT.md). We hold ourselves to a welcoming, respectful, and inclusive standard — both in code and in community.

---

## elizaOS Architecture Overview

MiladyAI agents run on **[elizaOS](https://github.com/elizaOS/eliza)**, the modular multi-agent runtime. Understanding elizaOS is essential before contributing. Here are the key primitives:

| Concept | Description |
|:--------|:------------|
| **AgentRuntime** | The core elizaOS engine — manages memory, plugins, and model calls |
| **Character File** | A `.json` config defining an agent's persona, plugins, clients, and model |
| **Plugin** | An elizaOS extension package that adds Actions, Providers, and/or Evaluators |
| **Action** | Executes when the elizaOS agent decides to do something (e.g., post, call API) |
| **Provider** | Injects real-time context into the elizaOS agent's memory at inference time |
| **Evaluator** | Validates or scores agent responses after generation |
| **Client** | Connects the elizaOS agent to an interface (Twitter, Discord, Telegram, etc.) |
| **Memory / RAG** | elizaOS's built-in vector memory for long-term knowledge retrieval |

> 📖 elizaOS documentation: [eliza.how](https://eliza.how) | [GitHub](https://github.com/elizaOS/eliza) | [Discord](https://discord.gg/elizaos)

---

## Getting Started

### Prerequisites

- **Node.js** >= 23 *(required by elizaOS runtime)*
- **pnpm** >= 9 *(elizaOS uses pnpm workspaces)*
- Basic familiarity with elizaOS character files and plugin structure

### Setup

```bash
# 1. Fork & clone
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME

# 2. Install dependencies (elizaOS pnpm workspace)
pnpm install

# 3. Configure environment
cp .env.example .env
# Set model provider keys (OpenAI, Anthropic, etc.) per elizaOS docs

# 4. Run your elizaOS agent locally
pnpm start --character="characters/milady.json"
```

The `--character` flag tells elizaOS which character file to load. All MiladyAI agents have their own character file in `characters/`.

---

## Building elizaOS Plugins for MiladyAI

The best contributions are new elizaOS-compatible plugins. All MiladyAI capabilities are packaged as elizaOS plugins registered in character files.

### Plugin Structure

```
packages/plugin-milady-example/
  src/
    index.ts          # Plugin export
    actions/          # elizaOS Actions
    providers/        # elizaOS Providers
    evaluators/       # elizaOS Evaluators
  package.json
  tsconfig.json
```

### Plugin Scaffold

```typescript
// src/index.ts
import { Plugin } from "@elizaos/core";
import { aestheticScoreAction } from "./actions/aestheticScore";
import { trendingProvider } from "./providers/trending";

export const miladyExamplePlugin: Plugin = {
  name: "milady-example",
  description: "Example MiladyAI plugin for elizaOS agents",
  actions: [aestheticScoreAction],
  providers: [trendingProvider],
  evaluators: [],
};

export default miladyExamplePlugin;
```

### Writing an elizaOS Action

```typescript
// src/actions/aestheticScore.ts
import { Action, IAgentRuntime, Memory, State, HandlerCallback } from "@elizaos/core";

export const aestheticScoreAction: Action = {
  name: "AESTHETIC_SCORE",
  description: "Scores an image or concept for aesthetic value using MiladyAI models",
  similes: ["rate this", "how aesthetic", "score the vibe"],

  validate: async (runtime: IAgentRuntime, message: Memory): Promise<boolean> => {
    // Check that the message contains something to evaluate
    return message.content.text.length > 0;
  },

  handler: async (
    runtime: IAgentRuntime,
    message: Memory,
    state: State,
    _options: unknown,
    callback: HandlerCallback
  ): Promise<boolean> => {
    // Your elizaOS action logic here
    const score = await runtime.evaluate(message, state);
    await callback({ text: `Aesthetic score: ${score}` });
    return true;
  },

  examples: [
    [
      { user: "user", content: { text: "rate this image" } },
      { user: "Milady", content: { text: "Aesthetic score: 9.2 / 10 ✦" } },
    ],
  ],
};
```

### Writing an elizaOS Provider

```typescript
// src/providers/trending.ts
import { Provider, IAgentRuntime, Memory, State } from "@elizaos/core";

export const trendingProvider: Provider = {
  get: async (runtime: IAgentRuntime, message: Memory, state?: State): Promise<string> => {
    // Return context string injected into the elizaOS agent's prompt
    const trending = await fetchTrending(); // your data source
    return `Current trending aesthetics: ${trending.join(", ")}`;
  },
};
```

### Register in a Character File

```json
{
  "name": "Milady",
  "plugins": [
    "@miladyai/plugin-example",
    "@elizaos/plugin-bootstrap",
    "@elizaos/plugin-image-generation"
  ],
  "modelProvider": "anthropic",
  "clients": ["twitter", "discord"]
}
```

> 📖 Full elizaOS plugin guide: [eliza.how/docs/core/plugins](https://eliza.how/docs/core/plugins)

---

## Character Files

MiladyAI agents are defined by elizaOS character files. When editing characters:

- Files live in `characters/`
- Follow the [elizaOS character schema](https://eliza.how/docs/core/characterfile)
- Key fields: `name`, `bio`, `lore`, `topics`, `style`, `plugins`, `modelProvider`, `clients`
- Test changes with `pnpm start --character="characters/YOUR_FILE.json"`
- Keep persona lore consistent with the MiladyAI brand voice

---

## Pull Request Process

1. Run the full test suite: `pnpm test`
2. Spin up the elizaOS agent locally and confirm no runtime errors
3. Update character files and docs if agent behavior changes
4. Fill out the PR template — include the elizaOS version tested against
5. Request review from at least one maintainer
6. Merged via **squash and merge**

---

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>
```

**Types:** `feat` · `fix` · `docs` · `chore` · `refactor` · `test` · `perf`

**Examples:**
```
feat(plugin-aesthetic): add elizaOS image-scoring action
fix(character): correct milady.json modelProvider config  
docs(eliza): update elizaOS setup instructions
chore(deps): bump @elizaos/core to latest
```

---

<div align="center">
<sub>
  MiladyAI runs on <a href="https://github.com/elizaOS/eliza">elizaOS</a> ·
  Questions? <a href="https://discord.gg/miladyai">Discord</a> ·
  <a href="https://github.com/orgs/milady-ai/discussions">Discussions</a>
</sub>
</div>
