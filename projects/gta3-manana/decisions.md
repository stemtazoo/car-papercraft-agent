# Decisions

## Geometry

初期共通ジオメトリは ratio-first で管理する。

| parameter | ratio |
|---|---:|
| length | 1.00 |
| width | 0.41 |
| height | 0.34 |
| wheelbase | 0.61 |
| front overhang | 0.20 |
| rear overhang | 0.19 |

A4試作時の暫定完成全長を 160 mm とした場合の目安:

- 全長 160 mm
- 全幅 約66 mm
- 全高 約54 mm
- ホイールベース 約98 mm
- 前オーバーハング 約32 mm
- 後オーバーハング 約30 mm

これらは実車寸法ではなく、参考画像から作るペーパークラフト用の初期設計値。

## Simplifications

ローポリ感を利用し、複雑な曲面を増やさない。

基本構成:
1. left side
2. right side
3. hood + windshield + roof + rear window + trunk を可能なら連続した上面ストリップ
4. front fascia
5. rear fascia
6. underbody / floor
7. wheels

初回は以下を印刷表現とする。

- ヘッドライト
- グリル
- テールランプ
- ナンバープレート
- 黒いバンパーモール
- ドア境界
- 窓枠

ミラーとマフラーは別部品にせず、省略または印刷表現を優先する。

## Layout

A4横向きを第一候補とする。

- 左右側面を同一長さで配置
- 上面ストリップの全長を側面と一致させる
- front/rear fascia の幅を上面最大幅と一致させる
- floor は最後に残った領域へ配置
- wheels は小パーツ領域へまとめる
- のりしろは側面側より上面ストリップ側を中心に付け、輪郭を崩しにくくする

初回は工作性を優先し、車体本体のパーツ数を増やしすぎない。
