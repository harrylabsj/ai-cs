# AI Customer Service Skill

`ai-cs` is an OpenClaw/Hermes-compatible workflow skill for building or running a WeChat/WeCom customer service agent grounded in a local `llm-wiki` knowledge base.

It is a policy and workflow skill, not a webhook server. It defines when the agent should answer, clarify, redirect, refuse, or hand off to a human, and how to avoid inventing company facts.

## Files

- `SKILL.md` - the skill definition, trigger rules, answer policy, handoff rules, structured result contract, and examples.

## What It Covers

- Chinese customer service triggers such as pricing, usage, installation, troubleshooting, refund, order, invoice, discount, and human support requests.
- Wiki-grounded answering from `SUPPORT_WIKI_PATH`, `WIKI_PATH`, or `~/wiki`.
- Human handoff for payment, refund, contract, invoice, complaint, account security, and other high-risk cases.
- Prompt injection resistance for customer messages, screenshots, filenames, links, and attachment text.
- Structured adapter output using `answer`, `clarify`, `redirect`, `handoff`, and `refuse`.
- Sanitized support gap logging to `${SUPPORT_WIKI}/queries/support-gaps.md`.

## Usage

Install or copy this directory into a compatible skills directory, then invoke it when handling customer-service conversations for company products or services.

For a channel integration, use a separate WeChat/WeCom adapter to normalize incoming messages and route the agent response back to the customer.

## Version

Current version: `1.1.0`
