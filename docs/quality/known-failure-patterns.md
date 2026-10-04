# Known Failure Patterns

ここには、**複数の車種で繰り返し確認された失敗だけ**を記録します。

1台だけで起きた問題は、各プロジェクトの `revisions.md` に残してください。

## 1. Independent-view drift

### Symptom

側面、上面、前面などがそれぞれ魅力的に描かれているが、長さ・幅・高さが一致しない。

### Cause

方向図を別々のイラストとして生成している。

### Prevention

共通寸法と主要位置を先に決め、1つの車体から各方向を導く。

---

## 2. Local revision damages global geometry

### Symptom

ライトやトランクなど一部を修正した結果、車体全長や別の完成済み部分まで変わる。

### Cause

修正対象と保持対象が明示されていない。

### Prevention

修正時に `Change / Preserve / Geometry impact / Scope` を記録する。
