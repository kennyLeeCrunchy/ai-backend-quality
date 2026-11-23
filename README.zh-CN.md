# AI 后端工程 Skill

[English](README.md)

`ai-backend-quality` 是一个通用的中文 Agent Skill，用于设计、实现、排查和审查后端服务及 AI 应用后端。它沿着一条真实请求追到数据写入、后台任务、模型调用或工具执行，帮助找到需要改动的位置，并用可观察的证据验收。

## 覆盖内容

- 反向代理、负载均衡、API 网关、部署与服务发现。
- 数据库一致性、缓存、会话、重试和可靠异步消息。
- API 状态与权限、文件与产物、任务恢复和 SSE 流式响应。
- 模型接入、Agent 工作流、工具授权和检索权限。
- 可观测性，以及覆盖失败、竞速和恢复的验证矩阵。

[`SKILL.md`](SKILL.md) 提供工作方式、通用规则和按场景查阅的入口。[服务入口与流量治理](references/service-entry.md) 是独立章节。[前后端交互契约](references/frontend-backend-contracts.md) 和[后端验证矩阵](references/verification-matrix.md) 可用来对齐接口行为与验收证据。

## 安装与使用

先克隆仓库。

```sh
git clone https://github.com/kennyLeeCrunchy/ai-backend-quality.git
```

将 `ai-backend-quality` 文件夹放入所用 Agent 工具配置的技能目录，保留根目录下的 `SKILL.md` 和 `references/`。随后在任务中按名称使用这个 Skill。

```text
用 ai-backend-quality 检查报告生成后端的重复建单、SSE 重连漏事件，以及工具重试是否会造成重复副作用。
```
