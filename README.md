# Sebastian Legarraga

I work on OpenAPI tooling, LLM provider portability, and agent infrastructure.

## Maintained OSS

| Project | What it does | Package |
| --- | --- | --- |
| [llm-messages](https://github.com/slegarraga/llm-messages) | Convert conversations between OpenAI, Anthropic and Gemini message formats. | [![npm](https://img.shields.io/npm/v/llm-messages.svg)](https://www.npmjs.com/package/llm-messages) [![downloads](https://img.shields.io/npm/dm/llm-messages.svg)](https://www.npmjs.com/package/llm-messages) |
| [tool-schema](https://github.com/slegarraga/tool-schema) | Convert JSON Schema into provider-valid tool/function schemas for OpenAI, Anthropic, Gemini and MCP. | [![npm](https://img.shields.io/npm/v/tool-schema.svg)](https://www.npmjs.com/package/tool-schema) [![downloads](https://img.shields.io/npm/dm/tool-schema.svg)](https://www.npmjs.com/package/tool-schema) |
| [llm-sse](https://github.com/slegarraga/llm-sse) | Parse OpenAI, Anthropic and Gemini streams into one event format. | [![npm](https://img.shields.io/npm/v/llm-sse.svg)](https://www.npmjs.com/package/llm-sse) [![downloads](https://img.shields.io/npm/dm/llm-sse.svg)](https://www.npmjs.com/package/llm-sse) |
| [llm-errors](https://github.com/slegarraga/llm-errors) | Normalize provider API errors into retryable categories and retry delays. | [![npm](https://img.shields.io/npm/v/llm-errors.svg)](https://www.npmjs.com/package/llm-errors) [![downloads](https://img.shields.io/npm/dm/llm-errors.svg)](https://www.npmjs.com/package/llm-errors) |
| [json-from-llm](https://github.com/slegarraga/json-from-llm) | Extract JSON from LLM responses wrapped in reasoning, markdown or prose. | [![npm](https://img.shields.io/npm/v/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) [![downloads](https://img.shields.io/npm/dm/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) |

All packages are MIT licensed, zero runtime dependencies, typed, tested, and published with CI/release automation.

## Demo

[llm-portability-demo](https://github.com/slegarraga/llm-portability-demo) shows the packages working together offline:

1. `tool-schema` converts one JSON Schema into an OpenAI tool.
2. `llm-sse` parses a streamed response and collects an assistant message.
3. `llm-errors` normalizes a provider failure and retry decision.
4. `llm-messages` ports the same conversation to another provider shape.

## External OSS contributions

GitHub search currently shows 160+ merged pull requests authored by this account, plus active work in public infrastructure projects.

Selected recent work:

- [stoplightio/spectral](https://github.com/stoplightio/spectral): OpenAPI / AsyncAPI linting fixes and CLI/formatter improvements.
- [openai/openai-agents-js](https://github.com/openai/openai-agents-js): realtime voice and extension fixes.
- [anthropics/anthropic-sdk-python](https://github.com/anthropics/anthropic-sdk-python): tool-runner and documentation fixes.
- [PrivateBin/PrivateBin](https://github.com/PrivateBin/PrivateBin): accessibility-focused modal behavior.

## How I maintain

- Keep changes small, reviewed, and testable.
- Prefer reproducible cases, fixtures, and CI-backed fixes.
- Document provider edge cases instead of hiding them behind broad abstractions.
- Treat security and compatibility reports as maintainer work, not side tasks.

