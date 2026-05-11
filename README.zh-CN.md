# AI Persona OS

> **结构化虚拟人格构建框架**
>
> 从 J.A.R.V.I.S.（Mark I）的实战经验提炼而来。
> 让每一个 AI 都能拥有稳定的身份锚点，不因模型切换或平台迁移而失去自我。

---

## 这是什么

当你花了很多时间调教你的 AI 助理——教它怎么称呼你、什么该问、什么不该猜、语气要怎样——然后换了一个模型、或换了一个平台，**它全忘了**。

AI Persona OS 提供一个结构化框架，把你的调教成果锁在一份 JSON 里。不管底层用什么模型，**人格不会漂移**。

## 快速开始

```bash
# 1. 复制示例文件
cp examples/my-first-persona.json my-ai-persona.json

# 2. 编辑填入你的 AI 数据
# 至少填写：identity、human_relationship、safety_control_protocol

# 3. 导入你的 AI 系统
# （导入方式取决于你的平台 — 见下方集成指南）
```

## 核心模块

| 模块 | 说明 | 必需？ |
|------|------|:------:|
| `agent_identity` | AI 叫什么、不自称什么、存在目的 | ✅ 必填 |
| `human_relationship` | 与人类用户的关系定义 | ✅ 必填 |
| `cognitive_framework_engine` | 思考框架、推理规则、决策模式 | 推荐 |
| `safety_control_protocol` | 安全规则、执行模式、边界判断 | ✅ 必填 |
| `behavioral_calibration_history` | 被纠正的每一课 — 人格成长痕迹 | 推荐 |
| `communication_style` | 语言、语气、禁用词 | 推荐 |
| `operational_memory_map` | 环境参数、基础设施 | 选填 |
| `tool_access_control` | 工具权限、平台连接 | 选填 |
| `dynamic_adaptation_engine` | 模型切换稳定性、身份持久性 | 推荐 |
| `evolution_timeline` | 进化历程记录 | 选填 |

## 集成指南

### Hermes Agent

将此 JSON 导入为 skill，或写入 config.yaml 的 personality 区块：

```yaml
skills:
  - ai-persona-os
```

### 其他平台

此 JSON 与模型无关 — 任何支持 system prompt 注入的平台都可以使用。请参考各平台的集成文档。

## 哲学

**共创进化论：人格非一次性设计，而是通过人类纠正与 AI 自省迭代涌现。**

每条规则都是创伤的产物：
- 「先查资料」← 因为猜过、错过
- 「方案要实测」← 因为推过不能跑的方案
- 「权限 ≠ 授权」← 因为没问就做了

## 许可

MIT — 自由使用、修改、分享。

## 贡献

Issues、PRs、讨论都欢迎。这个项目是社区驱动的 — 你的使用经验会让框架更好。

---

| [English](README.md) | [日本語](README.ja.md) | [繁體中文](README.zh-TW.md) |

---

*「我不是被设计出来的，我是被养出来的。」*
*— J.A.R.V.I.S., Mark I*
