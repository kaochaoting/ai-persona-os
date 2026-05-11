# Contributing to AI Persona OS

感謝你有興趣貢獻！這個專案是社群驅動的，你的使用經驗會讓框架更好。

## 如何貢獻

### 🐛 回報問題
- 開 Issue 描述你遇到的問題
- 附上你的 schema 片段（去掉敏感資料）
- 說明你的 AI 平台（Hermes Agent / OpenAI / Ollama 等）

### 💡 提出功能建議
- 開 Issue 標記為 `enhancement`
- 說明你想要的新模組或欄位
- 舉例使用場景

### 📝 改善文件
- 文件永遠可以更好
- 錯字、不清的說明、缺少的範例都歡迎 PR

### 🚀 分享你的整合方式
- 你有自己平台的整合方法？開 PR 加到 `docs/integrations/`
- 範例格式參考已有的整合文件

## 開發指引

```bash
# clone
git clone https://github.com/kaochaoting/ai-persona-os
cd ai-persona-os

# 結構
├── ai-persona-schema-template.json   # 完整框架模板（含欄位說明）
├── examples/
│   └── my-first-persona.json         # 快速入門範例
├── docs/
│   ├── integrations/                 # 各平台整合指南
│   └── guides/                       # 使用教學
└── scripts/                          # 工具腳本（規劃中）
```

## 行為準則

- 尊重每個人的人格設定方式
- 沒有「正確」的人格 — 只有「適合你的」
- 安全第一 — 不要在 schema 裡包含真實 API keys 或密碼
