# P-Tech

GTA FiveMの犯罪ギミックを練習するための、スマートフォン対応ミニゲーム集です。

トップ画面からゲーム選択へ進み、練習したいギミックを起動できます。各ゲームは独立しているため、今後も同じアプリと公開URLの中へ追加できます。

## Games

### P-Tech: CodeCracker

- 対象: ATM強盗
- 4桁の数字コードを推理
- 60秒制限

### P-Tech: ChainBraker

- 対象: オイルリグ強盗
- 11列 × 8行、赤 / 緑 / 青の3色
- 同色グループを消去
- 下詰め後に左詰め
- 30秒制限

### P-Tech: JumpingMaze

- 対象: オイルリグ強盗
- 7列 × 7行、数字は1〜3
- 数字ぶん右または下へジャンプ
- 5秒の記憶フェーズと30秒の追跡フェーズ
- ミス3回以内に右下へ到達すると成功

### P-Tech: CardMemory

- 対象: オイルリグ強盗
- 5枚の本物の番号と位置を記憶
- 偽番号を無視して色・図形に関する3問へ回答
- 5秒の記憶フェーズと15秒の回答フェーズ

### P-Tech: FlashGrid

- 対象: 汎用（`games.json` で変更可能）
- 7列 × 7行の点灯位置を記憶
- 4秒の記憶フェーズと10秒の再現フェーズ
- 正しい10マスをすべて選ぶと成功

### P-Tech: CircuitLink

- 対象: 汎用（`games.json` で変更可能）
- 8個の接続点をドラッグして配線を整理
- 交差している配線をリアルタイム表示
- 30秒以内にすべての交差を解消すると成功

### P-Tech: RapidSequence

- 対象: 汎用（`games.json` で変更可能）
- 4レーンを流れる20個の信号を追跡
- 画面タップとキーボード入力に対応
- ミス3回未満で全信号を処理すると成功

## Structure

```text
index.html                  P-Techタイトル / ゲーム選択
games/
  code-cracker/             CodeCracker本体と仕様
  chain-braker/             ChainBraker本体と仕様
  jumping-maze/             JumpingMaze本体と仕様
  card-memory/              CardMemory本体と仕様
  flash-grid/               FlashGrid本体と仕様
  circuit-link/             CircuitLink本体と仕様
  rapid-sequence/           RapidSequence本体と仕様
```

外部ライブラリとビルド作業は不要です。

## Edit game menu

ゲーム選択カードの表示は [`games.json`](./games.json) で管理します。

- `title`: ゲーム名
- `label`: `ATM` や `OIL RIG` などの分類表示
- `description`: ゲーム説明
- `href`: ゲームのURL
- `status`: `PLAYABLE` や `COMING SOON`
- `color`: カードのアクセントカラー
- `enabled`: `true` で起動可能、`false` で準備中

`title`、`label`、`description`、`status`、`color` が未設定の場合は、共通の初期文言や色を自動で使用します。
