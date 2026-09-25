<p align="center">
  <img src="assets/images/chapter-4.svg" alt="4. ブランチ操作の章扉">
</p>

# 4. ブランチ操作

> この章では「作業内容を分けるために別ブランチを作る」ための基本操作を学びます。

| 項目 | 内容 |
| --- | --- |
| 作業 | 作業内容を分けるために別ブランチを作る |
| 目的 | 主流の作業を壊さずに試験的な変更を進める |

## コマンド例

```bash
# 新しいブランチを作成して移動する
git switch -c feature/login

# すでにあるブランチへ移動する
git switch feature/login
```

## ポイント

新しいブランチを作ってそのまま移動するときは `git switch -c`、すでにあるブランチへ移動するときは `git switch` を使うと手順が分かりやすくなります。

[← マニュアルの目次に戻る](gitmanual.md)
