# Git マニュアル

> **はじめてのバージョン管理**
>
> 小さな変更を、安全に記録して共有するための実践ガイド

![ブランチを使ったGitの作業イメージ](images/git-branching.svg)

**基本をつかむ · 変更を記録する · チームと共有する**

---

## 目次

1. [Git のしくみ](#1-git-のしくみ)
2. [最初の準備](#2-最初の準備)
3. [変更を記録する](#3-変更を記録する)
4. [ブランチで作業する](#4-ブランチで作業する)
5. [リモートと共有する](#5-リモートと共有する)
6. [困ったときの確認](#6-困ったときの確認)

---

## 1. Git のしくみ

Git は、ファイルの変更を履歴として保存するバージョン管理システムです。いつ、何を変更したかを記録し、必要に応じて過去の状態を確認できます。

| 場所 | 役割 |
|:--|:--|
| **ワーキングツリー** | 編集中のファイルがある場所 |
| **ステージングエリア** | 次の記録に含める変更を選ぶ場所 |
| **ローカルリポジトリ** | コミット（変更の記録）を保存する場所 |
| **リモートリポジトリ** | チームと共有するリポジトリ |

基本の流れは **編集 → ステージ → コミット → 共有** です。

## 2. 最初の準備

### Git のユーザー情報を設定する

コミットに表示する名前とメールアドレスを設定します。通常は一度だけ行います。

```bash
git config --global user.name "あなたの名前"
git config --global user.email "you@example.com"
```

設定を確認するには `git config --global --list` を実行します。

### リポジトリを用意する

既存のプロジェクトを取得する場合：

```bash
git clone https://github.com/example/project.git
cd project
```

新しいフォルダでGitを始める場合：

```bash
git init
```

## 3. 変更を記録する

### 状態を確認してコミットする

`git status` は、変更されたファイルやステージ済みのファイルを確認する基本コマンドです。こまめに実行すると、意図しないファイルの記録を防げます。

```bash
git status
git add README.md
git status
git commit -m "READMEを更新"
```

`git add .` は現在のフォルダ以下の変更をまとめてステージします。コミット前に `git status` で対象を確認してください。コミットメッセージには変更の内容を短く書きます。

### 履歴を見る

```bash
git log --oneline
```

各行にコミットの短縮IDとメッセージが表示されます。詳しい差分は `git show` で確認できます。

## 4. ブランチで作業する

ブランチを使うと、既存の作業を保ったまま新しい機能や修正に取り組めます。

```bash
git switch -c feature/add-search
# ファイルを編集して、変更をコミットする
git switch main
git merge feature/add-search
```

`git switch -c` はブランチを作成して切り替えます。作業がまとまったら、取り込み先のブランチに切り替えて `git merge` します。共有ブランチの名前が `main` 以外の場合は、その名前を使ってください。

## 5. リモートと共有する

リモートリポジトリの変更を取り込み、作業を共有します。リモート名 `origin` は一般的な初期設定です。

```bash
git pull
git push
```

新しいブランチを初めて共有するときは、次のように上流ブランチを設定します。

```bash
git push -u origin feature/add-search
```

まだリモートを登録していない場合は、リポジトリのURLを指定します。

```bash
git remote add origin https://github.com/example/project.git
```

## 6. 困ったときの確認

| 確認したいこと | コマンド |
|:--|:--|
| ファイルの変更状況 | `git status` |
| コミットの一覧 | `git log --oneline` |
| リモートの登録先 | `git remote -v` |
| 変更内容 | `git diff` |

### コミット前に確認する

```bash
git diff
git diff --staged
git status
```

`git diff` は未ステージの変更、`git diff --staged` はステージ済みの変更を表示します。共有された履歴を書き換える操作や、変更を破棄する操作は影響範囲を確認してから実行してください。

---

**おぼえておきたい基本のリズム**

`git status` → `git add` → `git commit` → `git push`
