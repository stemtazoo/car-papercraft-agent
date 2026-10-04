# Decisions

## Geometry

初期共通ジオメトリは ratio-first で管理する。

| parameter | ratio |
|---|---:|
| length | 1.00 |
| width | 0.40 |
| height | 0.33 |
| wheelbase | 0.60 |
| front overhang | 0.21 |
| rear overhang | 0.19 |

A4試作時の暫定完成全長を 160 mm とした場合の目安:

- 全長 160 mm
- 全幅 約64 mm
- 全高 約53 mm
- ホイールベース 約96 mm
- 前オーバーハング 約34 mm
- 後オーバーハング 約30 mm

## Color and markings

- 車体色: くすんだ黄色
- 窓: 濃いグレー〜黒
- バンパー: グレー＋黒ライン
- 側面モール: 黒
- TAXIサイン: 黄色地に黒文字
- 「L.C.-TAXI」表記: 黒文字
- 料金表風ステッカー: 印刷表現

## Simplifications

基本構成:
1. left side
2. right side
3. hood + windshield + roof + rear window + trunk の連続上面ストリップ
4. front fascia
5. rear fascia
6. underbody / floor
7. wheels
8. TAXI roof sign

初回は以下を印刷表現とする。

- ヘッドライト
- グリル
- テールランプ
- ナンバープレート
- ドア境界
- ドアハンドル
- 側面モール
- 側面ロゴ
- 料金表ステッカー

ミラーは別部品にせず、省略または印刷表現を優先する。

## Roof sign

TAXIサインは車体本体と分離する。

- 低い台形箱形状
- 前後両面に TAXI
- 左右面は黄色無地
- 小さなのりしろを付ける
- ルーフ中央よりやや前寄りへ取り付ける

## Layout

A4横向きを第一候補とする。

- 左右側面は完全に同じ全長
- 上面ストリップ全長は側面と一致
- 前後面の幅は共通全幅と一致
- 前後面の高さは側面の接続高さと一致
- TAXIサインは独立小パーツ領域へ配置
- wheelbaseは左右側面で厳密に一致させる
- のりしろは上面ストリップ側を中心に付ける

以前のAdmiral試作で起きた前後面の寸法不整合を避けるため、front/rear fascia は見た目ではなく共通 Width × 接続高さから決める。