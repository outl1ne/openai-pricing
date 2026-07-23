# OpenAI Pricing

Up-to-date pricing structure for OpenAI APIs as of **July 23, 2026**.

This repository provides structured JSON data (`pricing.json`) for OpenAI model costs to help developers estimate API usage costs within their applications.

Pricing source information is sourced from official OpenAI API documentation: [https://openai.com/api/pricing](https://openai.com/api/pricing)

---

## 📅 Status (as of 23.07.2026)

All retired and deprecated legacy endpoints (such as `o1-mini`, `gpt-4.5-preview`, `davinci-002`, `babbage-002`) have been removed.

### Supported & Available Model Families

- **GPT-5.6 Series (July 2026 Flagships)**:
  - `gpt-5.6-sol` - Flagship reasoning & coding workhorse ($5.00 / 1M input, $30.00 / 1M output)
  - `gpt-5.6-terra` - Balanced production model ($2.50 / 1M input, $15.00 / 1M output)
  - `gpt-5.6-luna` - Fast & low-latency tier ($1.00 / 1M input, $6.00 / 1M output)
- **GPT-5.5 & GPT-5.4 Series**:
  - `gpt-5.5`, `gpt-5.5-pro`
  - `gpt-5.4`, `gpt-5.4-pro`, `gpt-5.4-mini`, `gpt-5.4-nano`
- **GPT-5 Series**:
  - `gpt-5`, `gpt-5-mini`, `gpt-5-nano`, `gpt-5-chat-latest`
- **GPT-4.1 & GPT-4o Series**:
  - `gpt-4.1`, `gpt-4.1-mini`, `gpt-4.1-nano`
  - `gpt-4o`, `gpt-4o-mini`, `chatgpt-4o-latest`, `gpt-4o-2024-08-06`, `gpt-4o-mini-2024-07-18`
- **Reasoning Models (o-series)**:
  - `o1`, `o1-pro`, `o3`, `o3-pro`, `o3-mini`, `o3-deep-research`, `o4-mini-deep-research`
- **Realtime & Audio APIs**:
  - `gpt-realtime-2.1`, `gpt-realtime-2.1-mini`
  - Text & Audio token tiers
- **Image & Video APIs**:
  - `gpt-image-2`, `gpt-image-1`
  - `sora-2`, `sora-2-pro` (per-second billing; API sunset September 24, 2026)
- **Embeddings & Audio**:
  - `text-embedding-3-small`, `text-embedding-3-large`, `whisper`, `tts`, `tts-hd`

---

## 🛠️ Data Structure (`pricing.json`)

- `models`: Input, cached input, output token costs per 1M tokens ($ USD) and `batchDiscount`.
- `flex-processing`: Discounted token rates for Flex capacity processing.
- `priority-processing`: High-throughput / priority queue token rates.
- `audio-tokens`: Input and output rates for audio token processing in Realtime/Audio APIs.
- `image-tokens`: Token pricing for image inputs/outputs.
- `tools`: Service costs (Code Interpreter, File Search, Web Search per 1k calls).
- `embedding` / `embedding-batch`: Standard and batch rates for embedding models.
- `video`: Per-second generation rates for Sora 2 tiers.
