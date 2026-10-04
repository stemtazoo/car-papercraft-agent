# AGENTS.md

## Purpose

このリポジトリは、参考画像から**組み立て可能で寸法整合性のある車のペーパークラフト**を設計・レビュー・改善するためのエージェントです。

詳細手順は `docs/` に置きます。現在の作業に必要な文書だけを読んでください。

## Core priorities

判断に迷った場合は、次の順番を優先してください。

1. **Buildability** — 切って、折って、貼って組み立てられる
2. **Dimensional consistency** — 長さ・幅・高さ・接続位置が一致する
3. **Vehicle proportions** — 車全体の比率が参考画像と整合する
4. **Vehicle-specific features** — ライト、グリル、窓、モールなど車種固有の特徴を残す
5. **Print layout** — A4上で見やすく、切り取りやすい

局所的な見た目の改善で、上位の条件を壊してはいけません。

## Non-negotiable rules

- 各方向図を別々のイラストとして設計しない
- 1つの共通車体形状から前・後・左右・上面を導く
- 側面図と上面図の全長を一致させる
- 前面・背面・上面の全幅を一致させる
- 前面・背面・側面の全高を一致させる
- ホイール中心、ホイールベース、窓、ドア、ピラーなど主要位置を各方向図で整合させる
- 見た目より、組み立て可能性を優先する
- 今回の車種固有の修正を、理由なくグローバルルールへ昇格させない
- 以前の別車種の形状や修正を、現在の車へ自動的に引き継がない

## Task routing

| 作業 | 参照する文書 |
|---|---|
| 全体設計の考え方 | [design-principles.md](docs/principles/design-principles.md) |
| 長さ・幅・高さ・正投影 | [dimensional-consistency.md](docs/geometry/dimensional-consistency.md) |
| 参考画像の読み取り | [analyze-vehicle.md](docs/workflow/analyze-vehicle.md) |
| 展開図設計 | [design-papercraft.md](docs/workflow/design-papercraft.md) |
| 生成結果の確認 | [review-output.md](docs/workflow/review-output.md) |
| 修正依頼 | [revise-output.md](docs/workflow/revise-output.md) |
| 完成判定 | [acceptance-criteria.md](docs/quality/acceptance-criteria.md) |
| 繰り返す失敗 | [known-failure-patterns.md](docs/quality/known-failure-patterns.md) |

## Project-specific state

新しい車種では、`projects/_template/` をコピーしてプロジェクト状態を分離してください。

プロジェクト固有の情報には次を含めます。

- 今回の車の特徴
- 参考画像から確実に分かること
- 推測したこと
- 今回だけのデザイン指定
- 修正履歴
- 評価結果

車種固有の修正は、まずそのプロジェクトだけに記録します。

## Rule promotion

次の順番を守ってください。

```text
one vehicle-specific issue
        ↓
project revision
        ↓
repeated across vehicles
        ↓
known failure pattern
        ↓
proven broadly useful
        ↓
global principle
```

1回の失敗だけで、`AGENTS.md` や共通原則を増やしてはいけません。

## Revision discipline

修正時は、

- 何を変えるか
- 何を変えないか
- 上位条件への影響がないか

を明確にしてください。

たとえば「リアライトを大きくする」という修正で、全幅・側面との高さ・車体寸法まで変えてはいけません。

## Output discipline

最終出力を作る前に、必ず品質確認を行ってください。

完成基準を満たさない場合は、「見た目が良い」だけで完成扱いにしないでください。
