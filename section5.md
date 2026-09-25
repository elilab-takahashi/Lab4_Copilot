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

`git restore file` は作業ツリーの変更を戻すときに使います。ステージングだけを取り消したいときは `git restore --staged file` を使い、作業ツリーに残したまま整理すると安全です。

[← マニュアルの目次に戻る](gitmanual.md)
