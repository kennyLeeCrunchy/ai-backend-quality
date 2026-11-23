# AI Backend Quality

[简体中文](README.zh-CN.md)

 This includes [`SKILL.md`](SKILL.md) and the reference chapters. This README provides an English overview.

AI Backend Quality is an Agent Skill for designing, implementing, debugging, and reviewing backend services and AI applications. It follows a real request from the service entry point through storage, background work, model calls, or tool execution. It helps choose the smallest appropriate change and verify the resulting behavior.
**The skill itself is written in Simplified Chinese.**

## Coverage

- Reverse proxies, load balancing, API gateways, deployment, and service discovery.
- Database consistency, caching, sessions, retries, and reliable asynchronous messaging.
- API state and permissions, uploads and artifacts, task recovery, and SSE streaming.
- Model integration, Agent workflows, tool authorization, and retrieval access.
- Observability and a verification matrix for failures, races, and recovery.

[`SKILL.md`](SKILL.md) provides the workflow and points to the relevant reference chapters. [Service entry and traffic management](references/service-entry.md) has its own chapter. The [frontend–backend contracts](references/frontend-backend-contracts.md) and [verification matrix](references/verification-matrix.md) connect implementation decisions to observable behavior.

## Installation and use

Clone the repository.

```sh
git clone https://github.com/kennyLeeCrunchy/ai-backend-quality.git
```

Place the `ai-backend-quality` folder in the skills directory configured by your agent tool, with `SKILL.md` and `references/` at its root. Then ask your agent to use the skill by name.

```text
Use ai-backend-quality to review our report-generation backend for duplicate task creation, missed SSE events, and unsafe tool retries.
```
