# Grok
高稳定、低延迟的全球全模型 AI API 中转平台
# 🚀 ClaudeMix - 高稳定、低延迟的全球全模型 AI API 中转平台

> **TL;DR**：针对开发者与企业打造的高可用 AI API 中转服务。完全兼容 OpenAI / Claude 官方接口。

**立即注册体验** → [https://www.claudemix.com/sign-up?aff=EOUT](https://www.claudemix.com/sign-up?aff=EOUT)

---

## ✨ 为什么选择 ClaudeMix？

在开发 AI 应用或自用客户端（如 NextChat、LobeChat、Claude Dev / Cursor 等）时，常常面临 API 接入难、网络不稳定、多模型切换繁琐等问题。

**ClaudeMix** 整合全球优质节点与渠道资源，提供统一的 API 接口，帮助开发者快速集成主流大语言模型。

---

## 🔥 核心特性

- **全模型覆盖**：同步支持 OpenAI、Anthropic（Claude）、xAI（Grok）、Google（Gemini）、DeepSeek、Midjourney 等主流模型
- **100% 协议兼容**：采用标准 OpenAI / Anthropic 格式，无缝替换原有 `base_url` 和 `api_key`
- **高可用与低延迟**：多机房负载均衡与智能化路由，节点自动容错切换，保障 99.9% 稳定 SLA
- **灵活透明计费**：按量扣费，无隐形消费，提供实时消耗明细与日志查询
- **支持高并发**：针对企业级场景优化并发限制，满足批量任务与高频调用需求

---

## 📦 支持模型一览

| 供应商 | 代表模型 | 适用场景 |
|--------|----------|----------|
| **OpenAI** | `gpt-6-astra`, `gpt-5.6-sol`, `gpt-5.6-terra`, `gpt-live-1` | 复杂推理、代码生成、代理任务、实时语音 |
| **Anthropic** | `claude-fable-5.1`, `claude-opus-5`, `claude-sonnet-5` | 编码辅助、长文本分析、高安全知识工作 |
| **xAI** | `grok-4.7`, `grok-4.6` | 编码与工程任务、长上下文知识问答 |
| **Google** | `gemini-3.8-flash`, `gemini-3.8-live`, `gemini-3.8-live-extended-thinking` | 超长上下文理解、多模态处理、实时对话 |
| **DeepSeek** | `deepseek-v4.1-flash`, `deepseek-chat`, `deepseek-coder` | 高性价比推理与代码构建 |
| **图像 / 多模态** | `midjourney`, `dall-e-3`, `whisper`, `gpt-image-2.5` | 图像生成、语音转文字、多模态创作 |

---

## ⚡ 快速接入示例

只需修改两行代码，即可无缝替换官方接口：

```python
from openai import OpenAI

client = OpenAI(
    api_key="sk-你的密钥",                    # 替换为 ClaudeMix 的 API Key
    base_url="https://api.claudemix.com/v1"   # 替换为 ClaudeMix 的 Base URL
)

response = client.chat.completions.create(
    model="gpt-6-astra",
    messages=[{"role": "user", "content": "你好，介绍一下你自己"}]
)

print(response.choices[0].message.content)
from anthropic import Anthropic

client = Anthropic(
    api_key="sk-你的密钥",
    base_url="https://api.claudemix.com"
)
