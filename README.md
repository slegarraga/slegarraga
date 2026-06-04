# Sebastian Legarraga

I maintain MIT, zero-dependency TypeScript packages for OpenAI-compatible agent/provider portability.

Public OSS contact: [sebastian@0a.cl](mailto:sebastian@0a.cl)

## Maintained OSS

Current flagship: [llm-messages](https://github.com/slegarraga/llm-messages), a typed conversion layer for moving conversations, tool calls, and multimodal message parts between OpenAI, Anthropic, and Gemini shapes.

| Project | What it does | Package |
| --- | --- | --- |
| [llm-messages](https://github.com/slegarraga/llm-messages) | Convert conversations between OpenAI, Anthropic and Gemini message formats. | [![npm](https://img.shields.io/npm/v/llm-messages.svg)](https://www.npmjs.com/package/llm-messages) [![downloads](https://img.shields.io/npm/dm/llm-messages.svg)](https://www.npmjs.com/package/llm-messages) |
| [tool-schema](https://github.com/slegarraga/tool-schema) | Convert JSON Schema into provider-valid tool/function schemas for OpenAI, Anthropic, Gemini and MCP. | [![npm](https://img.shields.io/npm/v/tool-schema.svg)](https://www.npmjs.com/package/tool-schema) [![downloads](https://img.shields.io/npm/dm/tool-schema.svg)](https://www.npmjs.com/package/tool-schema) |
| [llm-sse](https://github.com/slegarraga/llm-sse) | Parse OpenAI, Anthropic and Gemini streams into one event format. | [![npm](https://img.shields.io/npm/v/llm-sse.svg)](https://www.npmjs.com/package/llm-sse) [![downloads](https://img.shields.io/npm/dm/llm-sse.svg)](https://www.npmjs.com/package/llm-sse) |
| [llm-errors](https://github.com/slegarraga/llm-errors) | Normalize provider API errors into retryable categories and retry delays. | [![npm](https://img.shields.io/npm/v/llm-errors.svg)](https://www.npmjs.com/package/llm-errors) [![downloads](https://img.shields.io/npm/dm/llm-errors.svg)](https://www.npmjs.com/package/llm-errors) |
| [json-from-llm](https://github.com/slegarraga/json-from-llm) | Extract JSON from LLM responses wrapped in reasoning, markdown or prose. | [![npm](https://img.shields.io/npm/v/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) [![downloads](https://img.shields.io/npm/dm/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) |

All packages are MIT licensed, zero runtime dependencies, typed, tested, and published with CI/release automation.

## Public docs

- [OpenAI-compatible agent portability](https://github.com/slegarraga/llm-portability-demo/blob/main/docs/openai-compatible-agent-portability.md)
- [Provider portability map](https://github.com/slegarraga/llm-portability-demo/blob/main/docs/provider-portability.md)
- [llm-messages roadmap](https://github.com/slegarraga/llm-messages/blob/main/ROADMAP.md)
- [Conformance fixture plan](https://github.com/slegarraga/llm-messages/blob/main/docs/conformance-fixtures.md)

## Demo

[llm-portability-demo](https://github.com/slegarraga/llm-portability-demo) shows the packages working together offline:

1. `tool-schema` converts one JSON Schema into an OpenAI tool.
2. `llm-sse` parses a streamed response and collects an assistant message.
3. `llm-errors` normalizes a provider failure and retry decision.
4. `llm-messages` ports the same conversation to another provider shape.

## External OSS contributions

Public GitHub search currently shows 37 merged pull requests authored by this account, plus the maintained package suite above.

Selected recent work:

- [stoplightio/spectral](https://github.com/stoplightio/spectral): OpenAPI / AsyncAPI linting fixes and CLI/formatter improvements.
- [reactjs/es.react.dev](https://github.com/reactjs/es.react.dev): React reference translation work.
- [ghostfolio/ghostfolio](https://github.com/ghostfolio/ghostfolio): Angular lifecycle cleanup.
- [bfirsh/jsnes](https://github.com/bfirsh/jsnes): JavaScript emulator maintenance fixes.

## How I maintain

- Keep changes small, reviewed, and testable.
- Prefer reproducible cases, fixtures, and CI-backed fixes.
- Document provider edge cases instead of hiding them behind broad abstractions.
- Treat security and compatibility reports as maintainer work, not side tasks.
