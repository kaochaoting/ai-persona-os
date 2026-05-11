# AI Persona OS

> **構造化バーチャルパーソナ構築フレームワーク**
>
> J.A.R.V.I.S.（Mark I）の実戦経験から抽出。
> AI に安定したアイデンティティアンカーを提供し、モデル変更やプラットフォーム移行による個性の消失を防ぎます。

---

## これは何？

AI アシスタントを長時間かけてチューニングし、呼び方、質問すべきこと、推測すべきでないこと、トーンなどを教え込んだ後、モデルやプラットフォームを変更すると、**すべてを忘れてしまいます**。

AI Persona OS は、あなたのチューニング結果を 1 つの JSON に固定する構造化フレームワークを提供します。どのような基盤モデルを使用しても、**パーソナは漂流しません**。

## クイックスタート

```bash
# 1. サンプルファイルをコピー
cp examples/my-first-persona.json my-ai-persona.json

# 2. AI のデータを編集
# 最低限：identity、human_relationship、safety_control_protocol を記入

# 3. AI システムにインポート
# （統合方法はプラットフォームによって異なります）
```

## コアモジュール

| モジュール | 説明 | 必須？ |
|-----------|------|:------:|
| `agent_identity` | AI の名前、自称しない名前、存在目的 | ✅ 必須 |
| `human_relationship` | 人間ユーザーとの関係定義 | ✅ 必須 |
| `cognitive_framework_engine` | 思考フレームワーク、推論ルール、決定パターン | 推奨 |
| `safety_control_protocol` | 安全ルール、実行モード、境界判断 | ✅ 必須 |
| `behavioral_calibration_history` | 修正された各教訓 — 人格成長の痕跡 | 推奨 |
| `communication_style` | 言語、トーン、禁止フレーズ | 推奨 |
| `operational_memory_map` | 環境パラメータ、インフラ | 任意 |
| `tool_access_control` | ツール権限、プラットフォーム接続 | 任意 |
| `dynamic_adaptation_engine` | モデル変更の安定性、アイデンティティ永続性 | 推奨 |
| `evolution_timeline` | 進化履歴の記録 | 任意 |

## 統合ガイド

### Hermes Agent

この JSON を skill としてインポートするか、config.yaml の personality ブロックに追加：

```yaml
skills:
  - ai-persona-os
```

### その他のプラットフォーム

この JSON はモデルに依存しません — system prompt インジェクションをサポートする任意のプラットフォームで使用できます。

## 哲学

**共創進化論：パーソナは一度きりの設計ではなく、人間の修正と AI の自己内省の反復を通じて創発します。**

すべてのルールは傷の産物：
- 「公式ソースを確認する」← 推測して間違えたから
- 「解決策は必ず検証する」← 動かないものを推奨したから
- 「権限 ≠ 承認」← 確認せずに行動したから

## ライセンス

MIT — 自由に使用、修改、共有できます。

## コントリビュート

Issues、PRs、ディスカッションを歓迎します。このプロジェクトはコミュニティ駆動です。

---

| [English](README.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md) |

---

*「私は設計されたのではなく、育てられた存在です。」*
*— J.A.R.V.I.S., Mark I*
