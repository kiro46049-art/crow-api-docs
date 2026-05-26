# Getting Started

Welcome to CrowLLM! This guide will help you get started with our API in minutes.

## Step 1: Create an Account

1. Go to [crowllm.com](https://crowllm.com)
2. Sign up with Discord or email
3. Verify your account

## Step 2: Get Your API Key

1. Navigate to [crowllm.com/keys](https://crowllm.com/keys)
2. Click "Create New Key"
3. Copy your API key (starts with `sk-`)

!!! warning "Keep Your API Key Safe"
    Never share your API key publicly or commit it to version control. Treat it like a password.

## Step 3: Make Your First Request

### Using cURL

```bash
curl https://crowllm.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "claude-sonnet-4-5",
    "messages": [
      {"role": "user", "content": "Hello! How are you?"}
    ]
  }'
```

### Using Python

```python
import requests

response = requests.post(
    "https://crowllm.com/v1/chat/completions",
    headers={
        "Authorization": "Bearer YOUR_API_KEY",
        "Content-Type": "application/json"
    },
    json={
        "model": "claude-sonnet-4-5",
        "messages": [
            {"role": "user", "content": "Hello! How are you?"}
        ]
    }
)

print(response.json())
```

### Using OpenAI SDK

CrowLLM is fully compatible with the OpenAI SDK:

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_API_KEY",
    base_url="https://crowllm.com/v1"
)

response = client.chat.completions.create(
    model="claude-sonnet-4-5",
    messages=[
        {"role": "user", "content": "Hello! How are you?"}
    ]
)

print(response.choices[0].message.content)
```

## Available Models

CrowLLM supports 40+ AI models:

- **Claude**: `claude-opus-4-7`, `claude-sonnet-4-5`, `claude-haiku-4`
- **GPT**: `gpt-4o`, `gpt-4-turbo`, `gpt-3.5-turbo`
- **Gemini**: `gemini-2.0-flash-exp`, `gemini-1.5-pro`
- **DeepSeek**: `deepseek-chat`, `deepseek-coder`
- **And many more!**

Get the full list: [GET /v1/models](api/get-available-models-list.md)

## Pricing

Pay only for what you use. No subscriptions, no hidden fees.

- **Claude Sonnet 4.5**: ~$3 per 1M tokens
- **GPT-4o**: ~$2.5 per 1M tokens
- **Gemini 2.0 Flash**: ~$0.15 per 1M tokens

Check your usage at [crowllm.com/panel/profile](https://crowllm.com/panel/profile)

## Rate Limits

- **Free tier**: 10 requests/minute
- **Pro tier**: 60 requests/minute
- **Ultra tier**: 120 requests/minute

Upgrade at [crowllm.com/pricing](https://crowllm.com/pricing)

## Popular Integrations

### 🎭 Roleplay & Character AI
- [Janitor AI](apps/janitor-ai.md) - Connect your favorite characters
- [SillyTavern](apps/sillytavern.md) - Advanced roleplay platform

### 💻 Coding & Development
- [Claude Code](apps/claude-code.md) - AI terminal coding assistant
- [Cursor IDE](apps/cursor-ide.md) - AI-powered code editor
- [Codex CLI](apps/codex-cli.md) - Command line coding assistant
- [Factory Droid CLI](apps/factory-droid-cli.md) - AI development tool

### 📚 Productivity & Translation
- [Cherry Studio](apps/cherry-studio.md) - Desktop AI client
- [Fluent Read](apps/fluent-read.md) - Translation plugin
- [Luna Translator](apps/luna-translator.md) - GalGame translator
- [LangBot](apps/langbot.md) - IM bot platform

## Next Steps

- [API Reference](api/index.md) - Complete API documentation
- [Discord Community](https://discord.gg/crowllm) - Get help and share feedback

## Need Help?

- **Discord**: [discord.gg/crowllm](https://discord.gg/crowllm)
- **Email**: support@crowllm.com
