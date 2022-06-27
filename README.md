# git-practice-80
Gitの練習

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
