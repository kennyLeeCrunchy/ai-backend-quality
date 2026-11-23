# 来源与视频章节

视频用一个图书借阅系统解释生产服务的演进。以下是章节定位，技术选型和验收条件以当前项目为准。[图书借阅系统视频](https://www.douyin.com/video/7710506054701960463)

| 约略时段 | 视频演示 | 对应章节 |
|---|---|---|
| 06:00–09:45 | 从本机部署到服务端，垂直与水平扩展，反向代理、实例分流与摘除 | [服务入口与流量治理](service-entry.md) |
| 09:45–17:45 | 数据库瓶颈、主从延迟、旁路缓存与失效问题、多实例共享会话 | [数据库、缓存与会话](data-and-cache.md) |
| 20:00–23:45 | 环境不一致、镜像与容器、交付、灰度及回滚 | [部署与服务演进](deployment-and-service-evolution.md) |
| 23:45–32:50 | 单体的拆分条件、RPC 与 IDL、契约变更、容器编排和动态服务发现 | [部署与服务演进](deployment-and-service-evolution.md) |
| 32:50–36:30 | 连接池、超时、重复尝试引发级联故障、熔断、降级和舱壁隔离 | [容错与异步消息](resilience-and-messaging.md) |
| 36:30–39:50 | 外部统一入口、按服务路由、协议转换、鉴权限流和网关自身扩容 | [服务入口与流量治理](service-entry.md) |
| 39:50–44:00 | 通知等后续工作异步化，消息削峰、持久化、重复消费与幂等 | [容错与异步消息](resilience-and-messaging.md) |
| 44:00–46:40 | 指标发现异常、追踪定位慢调用、日志解释失败 | [可观测性与验证](observability-and-verification.md) |
| 46:40–49:55 | 服务网格的数据面和控制面，以及引入代理的运行成本 | [部署与服务演进](deployment-and-service-evolution.md) |

## 前后端契约和 AI 扩展

交互入口沿用 `ai-frontend-quality` 的 `references/frontend-backend-contracts.md` 所列场景，并在后端补充状态、权限、版本与恢复所需的实施规则。任务与 SSE 一章沿用其中 `references/backend-sse-contract.md` 的任务 ID、事件游标、快照和取消语义。双窗口保存、会话撤销、附件处理和内容预览继续与前端各自契约对齐。

Outbox、Worker 所有权、模型路由、工具审批、Agent 检查点和检索权限是基于服务工程原则增加的实现指引。协议细节以对应章节链接的标准为准。
