# AI Research Agent

An AI agent for market and audience research — web research with citations, document ingestion for RAG, and audience/persona profiling — backed by real web-search and document APIs.

Part of [Agency Agents OS](https://github.com/Anil-matcha/agency-agents-os), an open ecosystem of specialized AI agents for real business work.

## What this covers

This repo is the umbrella for anything an agency or in-house team would call "the AI research agent": answering a research question from live web sources with citations, turning PDFs and long documents into structured Markdown for RAG, and profiling a target audience's demographics, pain points, and language for a market/persona brief.

## Sub-agents

| Agent | Does | Status |
|---|---|---|
| [Web Research](agents/web-research/SKILL.md) | Synthesizes an answer to a research question from live web search across multiple sources, with citations | Coming Soon |
| [Document Ingestion](agents/document-ingestion/SKILL.md) | Converts PDFs and long documents into structured, RAG-ready Markdown with preserved structure | Coming Soon |
| [Audience Research](agents/audience-research/SKILL.md) | Profiles a target audience's demographics, pain points, and language for a market/persona brief | Coming Soon |

## Required Muapi APIs

- `research.web_search` — live multi-source web search and synthesis with citations.
- `research.pdf_to_markdown` — structured document-to-Markdown conversion for RAG pipelines.
- `research.audience_profile` — audience/persona profiling from web and market signals.

See each sub-agent's `SKILL.md` for the specific capabilities it uses.

## Setup

1. Create a Muapi account and API key at [muapi.ai](https://muapi.ai).
2. Review the [Muapi API quickstart](https://muapi.ai) and [OpenAPI schema](https://api.muapi.ai/openapi.json) for the research endpoints.
3. Load the `SKILL.md` for the sub-agent you need into your agent runtime (hosted agent, MCP client, or custom LLM app), or follow it manually.

## Read-only vs. write actions

All actions in this repo are `read-only`. Research, document conversion, and audience profiling produce files, Markdown, or reports — none of them write to or publish on any external system. Acting on the research (publishing, outreach, ad targeting) is out of scope; hand the output to the relevant agent for that step, with explicit approval.

## Status and limitations

All three sub-agents are Coming Soon. They depend on `research.web_search`, `research.pdf_to_markdown`, and `research.audience_profile`, none of which are yet live on Muapi. This repo documents the intended interface so agents and workflows can be built against it ahead of launch.

## Contributing

See [Agency Agents OS CONTRIBUTING.md](https://github.com/Anil-matcha/agency-agents-os/blob/main/CONTRIBUTING.md).

## License

[MIT](LICENSE)
