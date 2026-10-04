# Analyze Vehicle

参考画像から展開図を作る前に、まず車両そのものを分析します。

## 1. Identify available views

画像ごとに、

- front
- rear
- left side
- right side
- top
- front three-quarter
- rear three-quarter

のどれに近いか整理します。

## 2. Record reliable observations

直接確認できる特徴を記録します。

例:

- セダン / ワゴン / バン / リムジン
- 直線的 / 丸みが強い
- ボンネットが長い
- トランクが短い
- リアライトが側面まで回り込む
- グリルとライトが一体に見える

## 3. Estimate shared proportions

少なくとも、

- length : width : height
- wheelbase / length
- front overhang / length
- rear overhang / length

を意識します。

正確な実寸が分からない場合は、比率として扱います。

## 4. Separate uncertainty

見えない部分や画像間で矛盾する部分は、`observations.md` に「推測」として残します。

勝手に確定事項へ変えないでください。

## 5. Decide simplifications

紙で表現しにくい形状は、

- 平面化
- 面数削減
- 小部品の省略
- 印刷表現への置換

を検討します。

ただし、車種らしさを決める主要輪郭は維持します。
