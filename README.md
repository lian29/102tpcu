t

設定你的 git


git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global alias.st status
git config --global color.ui true
git init
git config --add core.quotepath false
git Alias 功能

使用終端機來操作 git 常會讓人覺得一直打指令很繁瑣，因此 git 也有提供 alias 的功能，例如你可以將 git status 縮寫為 git st，git checkout 縮寫為 git co 等，你只要這樣設定：

git config --global alias.st status

git 預設輸出是沒有顏色的，我們可以讓他在輸出時加上顏色讓我們更容易閱讀：

git config --global color.ui true

Git 顯示中文檔名

git 的一些指令 (如 status, diff) 在顯示非 ASCII 檔名有點問題, 會顯示成亂碼！ 有兩個方法解決

git config --add core.quotepath false
修改 ~/.gitconfig，找到 [core] 的位置後面，加上

[core]
    quotepath = false
如果還有問題，提醒在 bash 設定 export LANG=zh_TW.UTF-8

After doing this, you may fix the identity used for this commit with:

git commit --amend --reset-author
Git的基本功(status, .gitignore, add, commit, log)

git status

在一個 git 的 Repository 中你可以輸入git status來檢查目前 Git 的狀態

git status

設定不被追蹤的檔案(Untracked files) .gitignore


vi .gitignore
*.swp
*~
新增檔案(tracked files)，進入 stage 狀態

git add file.xxx

Create a new repository on the command line

當你建立新的 repository 時，會自動提示下列的指令


touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/yourname/xxx.git
git push -u origin master
Push an existing repository from the command line (git push)


git remote add origin https://github.com/petani/vim.git
git push -u origin master
你有兩種方法查看歷史紀錄

git log
git show HEAD 這個指令能顯示更詳細的變更內容
你可以使用 git blame 來查詢，誰把程式改到攔掉了！

git blame xxx.c
復原檔案, 這個方法很常用，但也很容易忽略。

git checkout 檔名 回復上一次 commit 的內容
get reset HEAD 檔名:
另一種受歡迎的版本控制系統

bitbucket.org
參考資料:

Git 教學(1) : Git 的基本使用
Git 教學(2)：Git Branch 的操作與基本工作流程
[Git] 從 Git 開始進入版本控制的世界 (Git in a Nutshell)
The four buckets — how Git considers content

