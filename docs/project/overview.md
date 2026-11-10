---
summary: Describes the project's durable purpose, boundaries, domain model, technology posture, architecture, and document ownership.
read_when:
  - onboarding to the project or evaluating whether a request belongs to its core domain
  - changing project purpose, scope boundaries, architecture, technology posture, or document ownership
  - needing stable project context that should not come from current-state.md
---

# Project Overview

## Project Card

- Name: `DeepSteer`
- Type: `macOS、iOS、Windows 三端原生远程 Agent 应用`
- Description: `制作 macOS、iOS、Windows 三端可用的原生应用，用于远程连接 dsh（DeepSeek Harness）实例，使移动终端无需直接通过 SSH 登录，即可利用服务器上的 Agent 执行任务。客户端通过 HTTPS/WSS 连接服务端网关；网关负责实例接入、会话管理与任务事件转发，dsh 负责服务器端 Agent 执行。具体 dsh 接入协议与能力边界在首个 SDD 中核验。`
- Current status: `docs/project/current-state.md`

## Scope Boundaries

- In scope: TBD - refine the project-owned responsibilities when they become concrete.
- Out of scope: TBD - record boundaries when exclusions become relevant.
- External dependencies: TBD - record dependencies when they become concrete.

## Domain Model

- Core concepts: TBD - define durable terms as the domain model stabilizes.
- Source of truth: TBD - define before introducing authoritative records or persistent data.
- Review boundary: TBD - define when a workflow requires human or external approval.

## Technology Posture

- Stack summary: `Apple 客户端：Swift + SwiftUI（macOS/iOS）；Windows 客户端：C# + .NET + WinUI 3（Windows App SDK）；服务端：Go 网关与 dsh 适配层；通信：HTTPS REST + WSS JSON 事件；协议契约：OpenAPI + JSON Schema；本地存储：SQLite，凭据使用系统安全存储。具体版本和 dsh 接入方式在首个 SDD 中核验并锁定。`

Use the stack summary for initialization. When the stack becomes concrete, keep a compact table here:

| Area | Choice | Owner Or Source |
| --- | --- | --- |
| Runtime and application | TBD | First accepted SDD spec or architecture decision |
| UI or interaction surface | TBD | First accepted SDD spec or architecture decision |
| Data and storage | TBD | First accepted SDD spec or architecture decision |
| Automation and integrations | TBD | First accepted SDD spec or architecture decision |
| Validation and delivery | TBD | `docs/workflow/` and accepted specs |

## Architecture Map

- System context: TBD - record external systems, major interactions, and trust boundaries when known.
- Major building blocks: TBD - link accepted specs or architecture documents when they exist.
- Runtime and deployment: TBD - link the owning spec when the project has a concrete runtime.

## Documentation Ownership

- Changing status: `docs/project/current-state.md`.
- Implementation contracts: `docs/specs/`.
- Workflow rules: `docs/workflow/`.
- Agent routing rules: `docs/.agent/conventions/`.
