<p align="center">
  <img src="assets/images/chapter-1.svg" alt="" width="1200" height="630">
</p>

# 1. リポジトリ作成

> この章では「新しい Git 管理を開始する」ための基本操作を学びます。

| 項目 | 内容 |
| --- | --- |
| 作業 | 新しい Git 管理を開始する |
| 目的 | 変更履歴を残す準備をする |

## コマンド例（このリポジトリだけ別のユーザー情報にしたい場合）

```bash
git init
git config user.name "名前"
git config user.email "a@example.com"
```

## ポイント

通常は、PC 全体で共通に使うユーザー名とメールアドレスを `--global` 付きで先に設定します。このコマンド例は、`git init` で作成したリポジトリだけ別の情報にしたい場合に行うローカル設定の例です。

[← マニュアルの目次に戻る](gitmanual.md)
