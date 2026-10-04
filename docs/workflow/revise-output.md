# Revise Output

修正では、現在うまくいっている部分をできるだけ保持します。

## Revision format

各修正について、次を整理します。

- Problem
- Change
- Preserve
- Geometry impact
- Scope

例:

```text
Problem:
Rear lights are too small.

Change:
Increase rear-light height slightly.

Preserve:
Body length, width, wheel position, roof, trunk.

Geometry impact:
Rear face and both side views must keep the same light height.

Scope:
This vehicle only.
```

## Do not over-correct

1つの細部を直すために、

- 全長
- 全幅
- 全高
- ホイールベース
- 他の完成済みパーツ

まで変更しないでください。

## Promotion rule

同じ失敗が別車種でも繰り返された場合だけ、`known-failure-patterns.md` への昇格を検討します。

1回の修正は、そのプロジェクトの `revisions.md` に残します。
