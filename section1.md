<p align="center">
  <img src="assets/images/chapter-1.svg" alt="1. リポジトリ作成の章扉" width="760">
</p>

# 1. リポジトリ作成

> この章では「新しい Git 管理を開始する」ための基本操作を学びます。

| 項目 | 内容 |
| --- | --- |
| 作業 | 新しい Git 管理を開始する |
| 目的 | 変更履歴を残す準備をする |

## コマンド例

```bash
git init
git config --global user.name "名前"
git config --global user.email "a@example.com"
```

## ポイント

`--global` を付けると、この PC で使う Git 全体にユーザー名とメールアドレスが適用されます。特定のリポジトリだけ別の情報にしたい場合は、同じ設定を `--local` 付きで上書きできます。

[← マニュアルの目次に戻る](gitmanual.md)
