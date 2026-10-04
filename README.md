# car-papercraft-agent

車の参考画像から、**実際に切って・折って・貼って組み立てられるペーパークラフト**を設計するためのエージェント用リポジトリです。

このリポジトリは、以前の長い単一プロンプトを分解し、

- 常に守る優先順位
- 寸法・正投影の原則
- 車両分析の手順
- 展開図設計の手順
- 出力レビュー
- 車種ごとの修正履歴

を分離して管理します。

## Core idea

```text
Reference images
      ↓
Vehicle analysis
      ↓
Shared geometry model
      ↓
Papercraft structure
      ↓
A4 layout
      ↓
Review
      ↓
Project-specific revision
```

重要なのは、各方向図を別々のイラストとして作らないことです。

**1つの車体形状を基準に、前・後・左右・上面を整合させ、その形状から工作可能な展開図を作る**ことを目標にします。

## Core priorities

優先順位は次です。

1. 組み立て可能であること
2. 寸法整合性
3. 車体プロポーション
4. 車種固有の特徴
5. 印刷レイアウトと見やすさ

局所的な見た目の修正で、上位の条件を壊してはいけません。

## Repository structure

```text
car-papercraft-agent/
├── AGENTS.md
├── README.md
├── docs/
│   ├── principles/
│   ├── geometry/
│   ├── workflow/
│   └── quality/
└── projects/
    └── _template/
```

## How to use

新しい車を作るときは、`projects/_template/` をもとに車種ごとのフォルダを作り、参考画像から分かった内容と修正履歴をそこへ記録します。

詳細な作業手順は [AGENTS.md](AGENTS.md) から必要な文書だけ参照してください。

## Origin

初期設計では、`stemtazoo/blog-instagram-prompts` の旧「車のペーパークラフトを作るプロンプト」で蓄積した要件を再整理しています。

旧プロンプトの内容をそのまま常時読み込ませるのではなく、再利用可能な原則と車種固有の修正を分離して運用します。
