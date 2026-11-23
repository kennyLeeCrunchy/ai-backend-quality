# AI Backend Quality

[简体中文](README.zh-CN.md)

**The Codex skill itself is written in Simplified Chinese.** This includes [`SKILL.md`](SKILL.md) and the reference chapters. This README provides an English overview.

AI Backend Quality is a Codex skill for designing, implementing, debugging, and reviewing backend services and AI applications. It follows a real request from the service entry point through storage, background work, model calls, or tool execution. It helps choose the smallest appropriate change and verify the resulting behavior.

## Coverage

- Reverse proxies, load balancing, API gateways, deployment, and service discovery.
- Database consistency, caching, sessions, retries, and reliable asynchronous messaging.
- API state and permissions, uploads and artifacts, task recovery, and SSE streaming.
- Model integration, Agent workflows, tool authorization, and retrieval access.
- Observability and a verification matrix for failures, races, and recovery.

[`SKILL.md`](SKILL.md) provides the workflow and points to the relevant reference chapters. [Service entry and traffic management](references/service-entry.md) has its own chapter. The [frontend–backend contracts](references/frontend-backend-contracts.md) and [verification matrix](references/verification-matrix.md) connect implementation decisions to observable behavior.

## Use in Codex

Clone the repository into your personal Codex skills directory so that `SKILL.md` sits directly in `ai-backend-quality`. For example, on Windows with the default user directory, run the following in PowerShell.

```powershell
git clone https://github.com/kennyLeeCrunchy/ai-backend-quality.git "$env:USERPROFILE/.codex/skills/ai-backend-quality"
```

In a Codex request, invoke the skill by name.

```text
$ai-backend-quality Review our report-generation backend for duplicate task creation, missed SSE events, and unsafe tool retries.
```
