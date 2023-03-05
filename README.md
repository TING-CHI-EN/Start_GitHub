# Start GitHub
// 其中 $ 為提示字元，在輸入指令時不用輸入該符號，否則會錯誤，若是使用 windows cmder 預設是 λ
# 顯示Git版本
$ git --version
# 第一步 
### 設定自己的名字和信箱
$ git config --global user.name "Your Name"

$ git config --global user.email "your@gmail.com"
### 確認是否輸入成功
$ git config --global user.name

$ git config --global user.email
### 删除設定
$ git config  --global --unset user.name

$ git config  --global --unset user.email
# 第二步 **git add**

### 將專案資料夾建立成 git repository
$ git init
### 也可以指定資料夾
$ git init directory
### 列出專案資料夾下的檔案和資料夾（-l 參數為列出詳細資料，-a 為列出隱藏資料夾）
$ ls -la
### 顯示目前工作環境狀態
$ git status
### 將檔案放進暫存區
$ git add 檔案
### 全部加入add
$ git add.
### 檔案尚未加入過追蹤時使用，即可恢復到檔案尚未加入暫存區
$ git rm --cached hello.py
### 若是要放棄修改可以使用 
$ git checkout -- 檔案名稱
### 比較現在檔案和上次 commit 之間的差異，也就是說你做了哪些修改，在git add之前用
$ git diff
# 第三步 **git commit**
### -m 為輸入 commit message，也就是說這個 commit 內做了哪些事情
$ git commit -m "message"
# 第四步 **git push**
### 本地端專案知道 origin 對應到遠端網址
$ git remote add origin 網址
### 將本地端程式 push 到遠端檔案庫(第一次)
$ git push -u origin master
### 第二次以上
$ git push
### 從 GitHub 下載回來
$ git pull
# 查看 Git 記錄相關操作
### 查看 Git config 設定
$ git config --list
### 查看目前工作目錄 (Working Directory) 中過去 Git commit 記錄
$ git log # 列出詳細的作者、時間、commit 內容

$ git reflog # 列出 commit 內容
### 查看目前 Remote 連線位置
$ git remote -v
### git 版本切換
$ git checkout <版本號> <省略 or 特定文件名稱>
# 其他
### 生成requirements.txt
pip freeze > requirements.txt
### 使用requirements.txt安裝
pip install -r requirements.txt


/* ======================================================= */ 
# 參考網址
https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/

https://hackmd.io/@ncrl-10/HkNA7sp0w 

https://hackmd.io/@sysprog/gnu-linux-dev/https%3A%2F%2Fhackmd.io%2F%40sysprog%2Fgit-with-github

https://www.maxlist.xyz/2018/11/02/git_tutorial/#3_git_commit_%E8%87%B3%E6%9C%AC%E5%9C%B0%E8%B3%87%E6%96%99%E5%BA%AB

/* ===================================================== */
# 未整理的地方

// 若檔案已經在 repository 內，則使用以下指令
repository 與 stage 的檔案都會被還原到 HEAD，但 working directory 內的檔案不變

$ git reset HARD

// SSH key 產生的方法

// 檢查是否有現存ssh key

$ ls -al ~/.ssh


$ ssh-keygen -t rsa -C "your@gmail.com"


$ ssh-agent bash


$ssh-add ~/.ssh/id_rsa


# 驗證你有沒有綁定

$ ssh -T git@github.com
