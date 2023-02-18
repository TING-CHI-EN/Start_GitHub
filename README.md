# Start GitHub

// 其中 $ 為提示字元，在輸入指令時不用輸入該符號，否則會錯誤，若是使用 windows cmder 預設是 λ

// 顯示Git版本

$ git --version
 
// 設定你的帳戶，讓 Git 知道這台電腦做的修改要連結到哪一個使用者（待會我們要在 Github 上註冊帳號，建議使用一致的帳號和電子信箱）

$ git config --global user.name "Your Name"

// 設定電子郵件

$ git config --global user.email "your@gmail.com"

// 删除設定

$ git config  --global --unset user.name
 
// 改變設定

$ git config --global user.name EasonHuang-tw

// 將專案資料夾建立成 git repository

$ git init

// 列出專案資料夾下的檔案和資料夾（-l 參數為列出詳細資料，-a 為列出隱藏資料夾）

$ ls -la

// 顯示目前工作環境狀態
 
$ git status

// 我們會發現因為我們有新增新的檔案，但是還沒進到 git 追蹤範圍中/暫存區，所以我們要使用 git add 加入追蹤，這樣之後檔案有修改就可以追蹤到。

$ git add 檔案

// 全部加入add

$ git add.
 
// 比較現在檔案和上次 commit 之間的差異，也就是說你做了哪些修改

 // 在git add之前用

$ git diff
 
// -m 為輸入 commit message，也就是說這個 commit 內做了哪些事情
 
$ git commit -m "message"

// 本地端專案知道 origin 對應到遠端網址
 
$ git remote add origin 網址
 
// 將本地端程式 push 到遠端檔案庫(第一次)

$ git push -u origin master

// 第二次以上

$ git pull

/* ======================================================= */
//查詢已建立的設定

git config --list
 
// 檔案尚未加入過追蹤時使用，即可恢復到檔案尚未加入暫存區
$ git rm --cached hello.py

// 若檔案已經在 repository 內，則使用以下指令
repository 與 stage 的檔案都會被還原到 HEAD，但 working directory 內的檔案不變

$ git reset HARD
 
參考網址

https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/

https://hackmd.io/@ncrl-10/HkNA7sp0w 
