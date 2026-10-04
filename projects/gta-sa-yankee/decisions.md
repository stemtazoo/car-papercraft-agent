# Decisions

## Geometry

Yankee は乗用車と異なり、1枚の連続上面ストリップよりも **cab + cargo box + chassis** の3構成に分ける。

初期共通ジオメトリ:

| parameter | ratio |
|---|---:|
| overall length | 1.00 |
| overall width | 0.28 |
| overall height | 0.38 |
| wheelbase | 0.56 |
| front overhang | 0.13 |
| rear overhang | 0.31 |
| cab length | 0.29 |
| cargo box length | 0.66 |
| cargo box width | 0.27 |
| cargo box height | 0.31 |
| cab height | 0.24 |

A4試作時の暫定完成全長を 180 mm とした場合の目安:

- 全長 180 mm
- 全幅 約50 mm
- 全高 約68 mm
- ホイールベース 約101 mm
- キャブ長 約52 mm
- 荷箱長 約119 mm
- 荷箱幅 約49 mm
- 荷箱高 約56 mm

## Structure

基本構成:
1. cab left side
2. cab right side
3. cab hood + windshield + roof strip
4. cab front fascia
5. cab rear wall
6. chassis / floor
7. cargo box side A
8. cargo box side B
9. cargo box roof
10. cargo box front wall
11. cargo box rear shutter
12. cargo box floor
13. wheels
14. optional mirrors

## Dimensional rules

- キャブ左右側面は完全に同じ全長・ホイール位置
- キャブ前面幅は共通 width から導く
- 荷箱前後面の幅は cargo box width と完全一致
- 荷箱左右側面の高さは cargo box height と完全一致
- 荷箱屋根幅は cargo box width と一致
- 荷箱屋根長は cargo box length と一致
- 荷箱後面シャッターは rear wall の内側表現とし、外形寸法を変えない
- シャーシ上の荷箱取付位置は左右で一致
- 後輪中心は左右完全一致
- キャブと荷箱を別々に“見た目で”スケーリングしない

## Simplifications

初回は以下を印刷表現とする。

- フロントグリル
- ヘッドライト
- 荷箱側面の汚れ
- 荷箱フレーム
- リアシャッターの横リブ
- ナンバープレート

サイドミラーは工作性が許せば別部品化する。

## Layout

Yankee は長いため、A4 1枚へ無理に収めない。
第一候補は A4 2枚構成。

- Sheet 1: cab + chassis + wheels
- Sheet 2: cargo box 6面 + mirror
- 両シートとも100%印刷前提
- 接続基準寸法を明記する

A4 1枚化のために全体比率や工作性を崩さない。