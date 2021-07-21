# 什麼是 git?  
  - 5W1H, 每樣東西都要先問 5W1H, 人事時地, 前因(Why)後果(How)
  - what 事: 什麼是git? 
  - who 人: 
  - when 時:
  - where 地:
  - why 因:
  - how 果:

# 什麼是 githab ? 

# 安裝

# 使用 
```
$ cd dir01
$ git init                (每一步都用 git status 看狀態)
$ git add .               (每一步都用 git status 看狀態) 
$ git remote add origin https://..........   
                          (設定目錄 code 放到github, 不行就先 git remote rm origin)
$ git commit -a -m "first"
$ git branch -M main      (設定主要分支爲 main)
$ git push -u origin main (把code 推送到 github, 之後就 只要 $git push 就好)
$ git pull                (把 code 從動 GitHub拉下來 )
```

# 4. 把 '程式碼' 'Code' 放到 internet (GitHub)
- Why: 這樣換電腦也可以找到你寫的 'code'
- Where: 
- How:
  1. `google git` **下載安裝`git`**, 很快很小, 然後重新開 `terminal` 測試 `$ git --version` 看到版本號 就對了
  2. `google github` 到 **github 網頁**, 建一個帳號, 登入
     - 建立一個**Repository (儲存位置)** 隨便叫做 **node123** 好了
     - 按 綠色的 `code` 按鈕, 會有 http 連結, 複製一下
  3. 
```
echo "# test01" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/dean0123/test01.git
git push -u origin main
```

# 把你寫的 'Web 網頁' 放到 internet, 這樣別的同學老師也可以看得到


# VSCode  (另外開Repository)
1. 安裝使用, 到 cd 工作目錄 下 打
``` 
$ code .
```

2. 安裝 相關的 外掛 (git, github, docker 等...)
   - git commit 可用 側邊, 然後選勾勾 按鈕 V 來 Commit 也要加 註解
   - git push 可選 git -> ... -> push 

   - Extensions 是左邊田字型按鈕 
    1. Remote  by Microdoft : 如果有Containder 用這個看remote code
    2. Docker  by Microsoft : 可以用這個啓動 管理 Docker
    3. Github  by Github : 可以 Pull request. 其實不用裝也可以用 Git Hub. 在Terminal 設定好就好了