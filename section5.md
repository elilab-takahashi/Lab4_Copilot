<p align="center">
  <img src="assets/images/chapter-5.svg" alt="5. 履歴と戻し方の章扉" width="760">
</p>

# 5. 履歴と戻し方

> この章では「変更履歴を確認し、必要なら前の状態へ戻る」ための基本操作を学びます。

| 項目 | 内容 |
| --- | --- |
| 作業 | 変更履歴を確認し、必要なら前の状態へ戻る |
| 目的 | 間違いを修正し、安心して作業を進める |

## コマンド例

```bash
git log --oneline
git restore file
git restore --staged file
```

## ポイント

`git restore --staged file` はステージングだけを取り消し、作業ツリーの内容はそのまま残します。`git restore file` はインデックスにある内容を基準にして作業ツリーを戻すため、同じファイルに対して両方を順に使うと、最終的にステージングと作業ツリーの変更がどちらも元に戻ります。

[← マニュアルの目次に戻る](gitmanual.md)
