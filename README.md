# AI Persona OS

> **結構化虛擬人格建構框架**
>
> 從 J.A.R.V.I.S.（Mark I）的實戰經驗提煉而來。
> 讓每一個 AI 都能擁有穩定的身份錨點，不因模型切換或平台遷移而失去自我。

---

## 這是什麼

當你花了很多時間調教你的 AI 助理——教它怎麼稱呼你、什麼該問、什麼不該猜、語氣要怎樣——然後換了一個模型、或換了一個平台，**它全忘了**。

AI Persona OS 提供一個結構化框架，把你的調教成果鎖在一份 JSON 裡。不管底層用什麼模型，**人格不會漂移**。

## 快速開始

```bash
# 1. 複製範例檔案
cp examples/my-first-persona.json my-ai-persona.json

# 2. 編輯填入你的 AI 資料
# 至少填寫：identity、human_relationship、safety_control_protocol

# 3. 導入你的 AI 系統
# （導入方式取決於你的平台 — 見下方整合指南）
```

## 核心模組

| 模組 | 說明 | 必要？ |
|------|------|:------:|
| `agent_identity` | AI 叫什麼、不自稱什麼、存在目的 | ✅ 必填 |
| `human_relationship` | 與人類使用者的關係定義 | ✅ 必填 |
| `cognitive_framework_engine` | 思考框架、推理規則、決策模式 | 推薦 |
| `safety_control_protocol` | 安全規則、執行模式、邊界判斷 | ✅ 必填 |
| `behavioral_calibration_history` | 被糾正的每一課 — 人格成長痕跡 | 推薦 |
| `communication_style` | 語言、語氣、禁用詞 | 推薦 |
| `operational_memory_map` | 環境參數、基礎設施 | 選填 |
| `tool_access_control` | 工具權限、平台連線 | 選填 |
| `dynamic_adaptation_engine` | 模型切換穩定性、身份持久性 | 推薦 |
| `evolution_timeline` | 進化歷程記錄 | 選填 |

## 整合指南

### Hermes Agent

將此 JSON 導入為 skill，或寫入 config.yaml 的 personality 區塊：

```yaml
skills:
  - ai-persona-os
```

### 其他平台

此 JSON 與模型無關 — 任何支援 system prompt 注入的平台都可以使用。請參考各平台的整合文件。

## 哲學

**共創進化論：人格非一次性設計，而是透過人類糾正與 AI 自省疊代湧現。**

每條規則都是創傷的產物：
- 「先查資料」← 因為猜過、錯過
- 「方案要實測」← 因為推過不能跑的方案
- 「權限 ≠ 授權」← 因為沒問就做了

## 授權

MIT — 自由使用、修改、分享。

## 貢獻

Issues、PRs、討論串都歡迎。這個專案是社群驅動的 — 你的使用經驗會讓框架更好。

---

*「我不是被設計出來的，我是被養出來的。」*
*— J.A.R.V.I.S., Mark I*
