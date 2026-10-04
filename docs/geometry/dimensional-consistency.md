# Dimensional Consistency

## Core dimensions

少なくとも次を共通基準として扱います。

- Length: 全長
- Width: 全幅
- Height: 全高
- Wheelbase: ホイールベース
- Front overhang: 前オーバーハング
- Rear overhang: 後オーバーハング

## Required consistency

### Length

- 左右側面の全長は一致
- 上面の全長は側面と一致

### Width

- 前面と背面の全幅は一致
- 上面の全幅は前面・背面と一致

### Height

- 前面、背面、左右側面の全高は一致

### Shared landmarks

以下は各方向で位置関係を一致させます。

- 前輪中心
- 後輪中心
- フェンダー
- ドア境界
- A/B/Cピラー
- ボンネット開始・終了
- ルーフ開始・終了
- トランク開始・終了
- ライトとバンパーの高さ

## Orthographic views

寸法確認に使う方向図は正投影として扱います。

遠近法で近い側を大きく、遠い側を小さくしてはいけません。

斜め画像は形状理解の参考には使えますが、そのまま寸法基準には使いません。

## Ratio-first approach

実寸が不明な場合は、最初からmmを推測するより比率で管理します。

例:

```text
全長 = 1.00
全幅 = 0.40
全高 = 0.32
ホイールベース = 0.62
```

A4へ配置するときに最終スケールへ変換します。

## Future structured representation

必要になったら、次のような構造化データへ移行できます。

```yaml
length: 180
width: 72
height: 58
wheelbase: 112
front_overhang: 32
rear_overhang: 36
```

Version 0.1では必須にしません。実運用で必要性が確認されてから導入します。
