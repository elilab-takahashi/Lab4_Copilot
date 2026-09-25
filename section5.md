<p align="center">
  <img src="assets/images/chapter-5.svg" alt="5. 履歴と戻し方の章扉">
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
git restore --staged file
git restore file
```

## ポイント

`git restore --staged file` はステージングだけを取り消し、作業ツリーの内容はそのまま残す独立した操作です。`git restore file` はインデックスにある内容を基準にして作業ツリーを戻すため、未コミットの変更内容は失われます。両方を戻したい場合は、先に `git restore --staged file`、次に `git restore file` の順で実行します。

[← マニュアルの目次に戻る](gitmanual.md)
