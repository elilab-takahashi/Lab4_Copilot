<p align="center">
  <img src="assets/images/chapter-1.svg" alt="1. リポジトリ作成の章扉">
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

まずは `--global` 付きでユーザー名とメールアドレスを設定しておくと、この PC で使う Git 全体に同じ情報を適用できます。特定のリポジトリだけ別の情報にしたい場合は、そのリポジトリ作成後に `--local` 付きで上書きします。

[← マニュアルの目次に戻る](gitmanual.md)
