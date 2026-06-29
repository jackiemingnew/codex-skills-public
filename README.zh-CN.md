# Codex Skills 公开索引

[English](README.md)

这是 Jackie 的 Codex skill 公开索引仓库。

这个仓库不保存任何 `skills/` 实体目录，只保存公开安全的分类、第三方来源、安装命令和恢复说明。真正的 skill 实体当前由私有管理仓库暂存，等明确决定公开源码后再迁移。

## 仓库关系

| 仓库 | 作用 |
| --- | --- |
| `codex-skills-public` | 公开索引，不存 skill 实体 |
| `codex-skills-private` | 私有管理仓库，暂存本地 skill 实体 |

## 这个仓库记录什么

| 分组 | 存储方式 | 用途 |
| --- | --- | --- |
| 可公开的本地 skill | 这里只做索引，实体暂存在私有仓库 | 自制或本地维护，后续可以选择公开 |
| 第三方 skill | 只记录来源和安装命令 | 从上游重新安装 |
| Codex 系统 skill | 只做说明 | 由 Codex 管理，不同步 |
| 必须私有的 skill | 只记录类别，不写具体名称 | 个人分身和本机监控类材料保持私有 |

## 可公开的本地 Skill

这些 skill 不是 private-only，但实体目前不发布在这个公开仓库：

| 分类 | Skills | 用途 |
| --- | --- | --- |
| dontbesilent 工作流 | `dbs`, `dbs-*` | 商业诊断、内容、目标、决策、对标、报告和学习 |
| 数字永生工具 | `immortal-skill` | 人格蒸馏框架和可复用模板 |
| 设计创作 | `design`, `design-system`, `brand`, `banner-design`, `ui-styling`, `slides`, `hatch-pet` | 品牌、UI、幻灯片、Banner、精灵图和视觉生产 |

## 按用途分四类

这是日常使用入口，借鉴 `write / draw / info / pm` 四类方案：

| 用途 | 含义 | 代表 skill |
| --- | --- | --- |
| `write` | 写作、改稿、内容、教学、叙事、表达 | `interview-me`, `idea-refine`, `spec-driven-development`, `documentation-and-adrs`, `dbs-content`, `dbs-content-system`, `dbs-hook`, `dbs-xhs-title`, `dbs-ai-check`, `brand`, `slides`, `teach`, `writing-great-skills` |
| `draw` | 设计、视觉、UI、Banner、幻灯片、生成资产 | `frontend-ui-engineering`, `design`, `design-system`, `banner-design`, `ui-styling`, `hatch-pet`, `ui-ux-pro-max`, `imagegen` |
| `info` | 查询、诊断、架构、领域理解、分析 | `using-agent-skills`, `context-engineering`, `source-driven-development`, `doubt-driven-development`, `browser-testing-with-devtools`, `debugging-and-error-recovery`, `code-review-and-quality`, `code-simplification`, `security-and-hardening`, `performance-optimization`, `observability-and-instrumentation`, `ask-matt`, `diagnosing-bugs`, `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, `ponytail-review`, `ponytail-audit`, `ponytail-debt`, `dbs-diagnosis`, `dbs-benchmark`, `dbs-deconstruct`, `openai-docs` |
| `pm` | 计划、项目管理、执行、状态、PRD、issue、triage、handoff | `planning-and-task-breakdown`, `incremental-implementation`, `test-driven-development`, `api-and-interface-design`, `git-workflow-and-versioning`, `ci-cd-and-automation`, `deprecation-and-migration`, `shipping-and-launch`, `dbs`, `dbs-action`, `dbs-goal`, `dbs-good-question`, `dbs-decision`, `dbs-save`, `dbs-restore`, `dbs-report`, `ponytail`, `ponytail-review`, `to-prd`, `to-issues`, `triage`, `tdd`, `implement`, `handoff` |

## 第三方来源

| 来源 | Skills | 用途 |
| --- | --- | --- |
| `mattpocock/skills` | `setup-matt-pocock-skills`, `ask-matt`, `grill-with-docs`, `grill-me`, `grilling`, `to-prd`, `to-issues`, `triage`, `tdd`, `diagnosing-bugs`, `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, `prototype`, `implement`, `resolving-merge-conflicts`, `handoff`, `teach`, `writing-great-skills` | 工程工作流、TDD、架构、PRD、issue、triage、handoff 和教学 |
| `ui-ux-pro-max` | `ui-ux-pro-max` | 可搜索的 UI/UX 设计知识库 |
| `DietrichGebert/ponytail` | `ponytail`, `ponytail-review`, `ponytail-audit`, `ponytail-debt`, `ponytail-gain`, `ponytail-help` | Codex 插件：YAGNI、标准库优先、最小正确实现和过度工程审查 |
| `addyosmani/agent-skills` | 从 `using-agent-skills` 到 `shipping-and-launch` 的 24 个生命周期 skill | 生产级工程纪律：spec、plan、build、test、review、安全、性能、可观测性和发布 |

## Codex 系统 Skill

这些由 Codex 自带，不通过这两个仓库同步：

- `imagegen`
- `openai-docs`
- `plugin-creator`
- `skill-creator`
- `skill-installer`

## 恢复方式

1. 克隆这个公开索引仓库。
2. 在可信机器上克隆私有管理仓库。
3. 从私有仓库恢复本地 skill：

```bash
cd ~/Documents/codex-skills-private
./scripts/sync-to-codex.sh
```

4. 第三方 skill 按 `catalog/sources.md` 或 `manifests/third-party.json` 重新安装。

## 安全边界

这个公开仓库不能包含：

- `skills/` 实体目录
- 个人分身或 digital-self 材料
- 本机 Codex 用量监控内部信息
- token、cookie、API key
- 原始或脱敏聊天语料路径
