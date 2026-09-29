# Build a Source-Grounded Market Brief

This walkthrough turns a broad market question into a concise brief whose claims can be checked. It follows the [Web Research skill](../agents/web-research/SKILL.md).

## Example request

> Compare the main scheduling tools for independent fitness studios in the United States. Focus on pricing, integrations, and recurring customer complaints. Cite sources and flag anything you cannot verify.

## Before you start

The research endpoints described by this repo are currently marked **Coming Soon**. First check the host for `research.web_search` and verify that it works. If it is unavailable, do not imply a live search happened: ask for source links/files or return a research plan until an approved live source is connected. Document ingestion is also a separate, not-yet-live capability; a user-provided document can still be analyzed if the host can read it.

## Workflow

1. **Narrow the question.** Confirm geography, audience, date range, and the decision the brief should support. Split it into sub-questions: candidate products, current pricing, integration coverage, and user-reported pain points.
2. **Gather evidence by sub-question.** Search each one independently. Keep the source URL, title, publisher, and published or accessed date with every result. Prefer primary pricing/product pages for vendor claims and attributable review sources for customer complaints.
3. **Check the evidence.** Seek independent corroboration for material claims. Keep one-source claims marked as such. If two sources disagree, report both values and their dates rather than choosing one silently. Treat an absent result as unknown, not proof that a product or feature does not exist.
4. **Separate observation from interpretation.** “The pricing page lists…” is an observation. “This may fit smaller studios…” is an inference and should be labeled as one, with its reason.
5. **Write the brief.** Lead with the answer, then include a comparison table, the strongest evidence, open questions, and source links. State the research date and the scope searched.

## Output checklist

- Scope: audience, geography, date range, and research date.
- Findings: each current factual claim linked to its source.
- Conflicts and single-source claims called out.
- Inferences labeled and separated from sourced facts.
- Gaps and failed searches listed explicitly.
- No inferred market share, pricing, or customer sentiment from incomplete samples.

## If the live search capability is unavailable

Say so before presenting findings. Offer to work from user-supplied links or files and label that result as source-limited. Do not fill the gap with model memory presented as current research.
