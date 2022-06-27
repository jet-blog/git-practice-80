# git-practice-80

## 初期設定
```bash
# ユーザー設定
git config --global user.name "UserName"
git config --global user.name "jet-blog"

# ユーザー確認
git config --global user.name

# メールアドレス設定
git config --global user.email "email@example.com"
git config --global user.email "y.yasson.n@gmail.com"

# メールアドレス確認
git config --global user.email
```

## 基礎知識
- originとは
  - リモートリポジトリのアクセス先に対してGitがデフォルトでつける名前です。

```bash
# originのアクセス先を確認するコマンド
git remote -v

origin  https://github.com/jet-blog/git-practice-80.git 
```

## 基本操作
```bash
# Gitリポジトリ作成
git init

# Gitリポジトリのダウンロード
git clone [リモートリポジトリのURL]

# 状態確認
git status

# Staging(ステージング)
git add ファイル名
git add .

# Commit(コミット)
git commit -m "コメント"

# Push(プッシュ)
git push origin [リモートブランチ名]
git push origin main
git push -u origin main
git push

# Pull(プル)
git pull origin [リモートブランチ名]
git pull origin main
git pull -u origin main
git pull

# Fetch(フェッチ)
git fetch

# ブランチの状態確認
git branch
git branch -a

# ブランチ作成
git branch ブランチ名
git branch develop

# ブランチの切替
git switch -C ブランチ名
git switch -C develop

# 差分確認
git diff
git diff --cached

# コミットログ参照
git log
git log --oneline

```

## ローカルリポジトリを後からリモートリポジトリにPUSHする方法

```bash
# Gitリポジトリ作成
git init

# ブランチ名変更
git branch -m main

# 管理対象ファイル作成
touch textA.txt

# ステージング
git add .

# コミット
git commit -m "textA.txt追加"

# リモートリポジトリの設定
git remote add origin git@GitHub.com:jet-blog/git-practice-80.git
git fetch origin
git rebase origin/main

# リモートリポジトリの確認
git remote -v

# Push
git push origin main

# 「-u」オプションで移行「git push」だけでpushできる
# 「origin main」を省略できる
git push -u origin main

# Push
git push
```
