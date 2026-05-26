# Welcome to CrowLLM API Documentation

Access 40+ AI models through one unified API.

## Quick Start

1. **Sign up** at [crowllm.com](https://crowllm.com)
2. **Get your API key** from [crowllm.com/keys](https://crowllm.com/keys)
3. **Make your first request**:

```bash
curl https://crowllm.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "claude-sonnet-4-5",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

## Features

- **40+ AI Models** - Claude, GPT-4, Gemini, DeepSeek, and more
- **OpenAI Compatible** - Drop-in replacement for OpenAI API
- **Pay As You Go** - No subscriptions, only pay for what you use
- **Fast & Reliable** - Global infrastructure with 99.9% uptime

## Popular Use Cases

### 🎭 Roleplay & Character AI
Connect with [Janitor AI](apps/janitor-ai.md), [SillyTavern](apps/sillytavern.md), and other character AI platforms.

### 💻 Coding & Development
Integrate with [Claude Code](apps/claude-code.md), [Cursor IDE](apps/cursor-ide.md), [Codex CLI](apps/codex-cli.md), and more.

### 📚 Productivity & Translation
Use with [Cherry Studio](apps/cherry-studio.md), [Fluent Read](apps/fluent-read.md), [Luna Translator](apps/luna-translator.md), and other tools.

## Need Help?

- [Getting Started Guide](getting-started.md)
- [API Reference](api/index.md)
- [Discord Community](https://discord.gg/crowllm)
