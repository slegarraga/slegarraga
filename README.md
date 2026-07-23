# Sebastian Legarraga

I maintain small, typed, zero-runtime-dependency TypeScript tools for portable
LLM agents across OpenAI, Anthropic, Gemini, and OpenAI-compatible APIs.

Public OSS contact: [sebastian@0a.cl](mailto:sebastian@0a.cl)

## Maintained OSS

Primary project: [llm-messages](https://github.com/slegarraga/llm-messages), a
typed conversion layer for moving conversations, completed Responses API
output, tool calls, and multimodal message parts between OpenAI, Anthropic, and
Gemini shapes.

| Project                                                      | What it does                                                                                          | Package                                                                                                                                                                                                            |
| ------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [llm-messages](https://github.com/slegarraga/llm-messages)   | Convert conversations and completed responses between OpenAI, Anthropic, and Gemini formats.          | [![npm](https://img.shields.io/npm/v/llm-messages.svg)](https://www.npmjs.com/package/llm-messages) [![downloads](https://img.shields.io/npm/dm/llm-messages.svg)](https://www.npmjs.com/package/llm-messages)     |
| [llm-sse](https://github.com/slegarraga/llm-sse)             | Normalize OpenAI Responses and Chat Completions, Anthropic, and Gemini SSE streams.                   | [![npm](https://img.shields.io/npm/v/llm-sse.svg)](https://www.npmjs.com/package/llm-sse) [![downloads](https://img.shields.io/npm/dm/llm-sse.svg)](https://www.npmjs.com/package/llm-sse)                         |
| [tool-schema](https://github.com/slegarraga/tool-schema)     | Convert JSON Schema into provider-valid tool/function schemas for OpenAI, Anthropic, Gemini, and MCP. | [![npm](https://img.shields.io/npm/v/tool-schema.svg)](https://www.npmjs.com/package/tool-schema) [![downloads](https://img.shields.io/npm/dm/tool-schema.svg)](https://www.npmjs.com/package/tool-schema)         |
| [llm-errors](https://github.com/slegarraga/llm-errors)       | Normalize provider API errors into retryable categories and retry delays.                             | [![npm](https://img.shields.io/npm/v/llm-errors.svg)](https://www.npmjs.com/package/llm-errors) [![downloads](https://img.shields.io/npm/dm/llm-errors.svg)](https://www.npmjs.com/package/llm-errors)             |
| [json-from-llm](https://github.com/slegarraga/json-from-llm) | Extract JSON from LLM responses wrapped in reasoning, markdown or prose.                              | [![npm](https://img.shields.io/npm/v/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) [![downloads](https://img.shields.io/npm/dm/json-from-llm.svg)](https://www.npmjs.com/package/json-from-llm) |

All five packages are MIT licensed, typed, tested, published with automated
releases, and have zero runtime dependencies.

## End-to-end proof

[llm-portability-demo](https://github.com/slegarraga/llm-portability-demo) runs
the suite together offline, with a committed deterministic transcript:

1. `json-from-llm` recovers a structured agent plan.
2. `tool-schema` produces OpenAI, Anthropic, Gemini, and MCP tool schemas.
3. `llm-sse` parses typed OpenAI Responses events and collects a function call.
4. `llm-errors` turns a rate limit into an explicit fallback decision.
5. `llm-messages` ports the same history to Anthropic and Gemini bodies.

No API key or network call is required for the conformance path.

## Maintenance evidence

- [Provider portability map](https://github.com/slegarraga/llm-portability-demo/blob/main/docs/provider-portability.md)
- [OpenAI-compatible agent portability](https://github.com/slegarraga/llm-portability-demo/blob/main/docs/openai-compatible-agent-portability.md)
- [llm-messages roadmap](https://github.com/slegarraga/llm-messages/blob/main/ROADMAP.md),
  [governance](https://github.com/slegarraga/llm-messages/blob/main/GOVERNANCE.md),
  and [support policy](https://github.com/slegarraga/llm-messages/blob/main/SUPPORT.md)
- [Public conformance fixtures](https://github.com/slegarraga/llm-messages/blob/main/docs/conformance-fixtures.md)
- [llm-messages releases](https://github.com/slegarraga/llm-messages/releases) and
  [llm-sse releases](https://github.com/slegarraga/llm-sse/releases)

## External OSS contributions

Accepted contributions span dozens of public repositories. Selected work:

- [reactjs/es.react.dev](https://github.com/reactjs/es.react.dev/pulls?q=is%3Apr+author%3Aslegarraga+is%3Amerged):
  React reference translation work.
- [ghostfolio/ghostfolio](https://github.com/ghostfolio/ghostfolio/pulls?q=is%3Apr+author%3Aslegarraga+is%3Amerged):
  Angular lifecycle and cleanup fixes.
- [stoplightio/spectral](https://github.com/stoplightio/spectral/pulls?q=is%3Apr+author%3Aslegarraga):
  OpenAPI/AsyncAPI linting and CLI work.
- [bfirsh/jsnes](https://github.com/bfirsh/jsnes/pulls?q=is%3Apr+author%3Aslegarraga+is%3Amerged):
  JavaScript emulator maintenance fixes.

## How I maintain

- Keep changes small, reviewed, and testable.
- Prefer reproducible cases, fixtures, and CI-backed fixes.
- Document provider edge cases instead of hiding them behind broad abstractions.
- Treat security and compatibility reports as maintainer work, not side tasks.
