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
git config --local user.name "名前"
git config --local user.email "a@example.com"
```

## ポイント

この例では、`git init` でリポジトリを作成したあとに、そのリポジトリで使うユーザー名とメールアドレスを `--local` 付きで設定しています。PC 全体で共通の設定を先に済ませたい場合は、同じ項目を `--global` 付きで登録できます。

[← マニュアルの目次に戻る](gitmanual.md)
