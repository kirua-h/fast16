# アーキテクチャ

## 全体構成

```
UI
↓
コンポーネント
↓
Hooks
↓
ストレージ・ユーティリティ
```

---

## フォルダ構成

```
app/
components/
hooks/
storage/
utils/
types/
assets/
```

---

## 各フォルダの役割

### app

画面定義を管理します。

---

### components

再利用できるUIコンポーネントを配置します。

例

- Header
- Countdown
- MealButton
- StatusCard
- MealInfo

---

### hooks

ロジックを管理します。

例

- useCountdown

UIの処理は書きません。

---

### storage

ローカル保存を担当します。

- 保存
- 読み込み

AsyncStorageを使用します。

---

### utils

共通処理を配置します。

例

- 残り時間計算
- 次回食事時刻計算
- 日付フォーマット

ストレージにはアクセスしません。

---

# データの流れ

```
食事開始ボタン

↓

現在時刻取得

↓

AsyncStorageへ保存

↓

状態更新

↓

残り時間再計算

↓

画面更新
```

---

# 状態管理

MVPでは

lastMealTime

のみ管理します。

React標準のstateで十分です。

---

# コンポーネント構成

```
HomeScreen

├── Header
├── StatusCard
├── Countdown
├── MealInfo
└── MealButton
```

---

# 設計方針

- 1コンポーネント1責務
- TypeScriptを使用
- 関数コンポーネントを使用
- 重複コードを書かない
- 可読性を優先する

---

# 将来追加予定

- 履歴
- 体重管理
- ウィジェット
- HealthKit
- Apple Watch
- グラフ
