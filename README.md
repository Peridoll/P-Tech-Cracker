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
- 今後追加予定

## Structure

```text
index.html                  P-Techタイトル / ゲーム選択
games/
  code-cracker/             CodeCracker本体と仕様
  chain-braker/             ChainBraker本体と仕様
```

外部ライブラリとビルド作業は不要です。
