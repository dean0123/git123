# 什麼是 git?  
  - 5W1H, 每樣東西都要先問 5W1H, 人事時地4w, 前因(Why)後果(How)
  - what 事: 什麼是git? 
  - who 人: 
  - when 時:
  - where 地:
  - why 因:
  - how 果:

# 什麼是 github?  跟 git 一樣嗎? 
- git 是一種**版本控制**的東西, 等於是**存檔**的概念, 
  - 就好象玩 game 可以存檔, 下次繼續玩一樣.  git 還可以存很多次, 就好象玩 game 可以在第三關存一次, 第五關存一次, 之後每關都會存, 等到打到第八關的時候, 發現其實第六關就走錯了, 這個時候, 就可以把第五關叫出來, 從第五關開始打. 
  - git 也是一樣, 寫程式每次**改完了一版**, 測試完了以後, 都要**養成好習慣 用 git 存起來**. 以免殺錯了檔案  或改錯了 從的 , 都可以從之前的某個存檔的版本叫出來.  所以要養成好的習慣, 在一開始寫 code 或是其他文件的時候, 就先設定用 git 來做版本控制與存檔. 
  - git 還有特異功能, 讓多人一起玩, 就像兩人一組一起闖關, 有人得到3個寶石存檔, 另外的人得到5個子彈存檔, 這樣你們一起的進度就會有3個寶石與5個子彈, git 也可以人讓多人一起開發code, 然後把之後多人修改的從的 code, merge 組合成一個共同的 code. 這個以後再慢慢了解. 
  
- github 是把 git code 存放在雲端的一個服務. 
  - git 本來是把 code 是放在本機自己用, 但是去了學校公司, 換了電腦, 換了地方, 就拿不到code, 也不能多人共用一起開發.  
  - github 是一個**雲端網頁的 git 服務**, 想像成 git 雲端的 hub, 透過 git 可以把本機的 code 指定放到雲端的 github 裏面, 這樣走到哪裏就都可以繼續 code 的開發, 也可以多人共用. 也不怕換電腦了. 除了 github, 還有很多其他的 git 雲端服務, 像是 gitlab, heroku 等等
  - github 除了放 code, 還可以把相關的專案, 文件, 說明, 網頁都放在這裏, 像是這一片文章就是 github 的一個說明檔 README.md 作出的靜態網頁. 


# 安裝
- git 需要安裝, `google git` 找到就可以**下載 git 安裝**了, 很快很小, 裝好後重開`Terminal` 下指令測試一下
```
$ git --version      (有版本號碼出來就對了) 
```
- github **不用安裝**, `google github` 找到 github 網頁去申請一個帳號密碼, 然後就可以使用了, 可以
  1. 登入後, 建立一個 **repository (儲存位置)** , 先叫做 **test123** 好了, 用來裝你的程式
  2. 按 綠色的 `code` 按鈕, 會看到 repository 的 http 連結. 複製一下等下 git 要用來 設定 remote 的存放點. 

# 使用 
```
$ cd dir01                (每個工作目錄, Project 都要單獨設定一次, )
$ git init                (把這個目錄 git 初始化, 每一步都用 git status 看狀態)
$ git add .               (加檔案到 git stage, 每一步都用 git status 看狀態) 
$ git remote add origin https://github.com/你的帳號名稱/test123.git  (<-- 貼上剛剛複製的連結)
                          (設定 git 目錄 code 放到 github, 不行就先 git remote rm origin)
$ git commit -a -m "first"
$ git branch -M main      (設定 code 主要分支爲 main)
$ git push -u origin main (把 code 推送到雲端 github, 之後就 只要 $git push 就好)
$ git pull                (把 code 從雲端 GitHub 拉下來 )
```


# 如何把 各自的 github repository 變成各自單獨網頁
- github 裏面 選 repositoty 後, 選 settings 設定, 左邊下面有個 pages 點開, 
- 然後 source 選 main 目錄 選 /root
- choose theme 選第一個, 
# 如何把 自己的 github root 變成網頁主頁

# VSCode  (另外開Repository)
1. 安裝使用, 到 cd 工作目錄 下 打
``` 
$ code .
```

2. 安裝 相關的 外掛 (git, github, docker 等...)
   - git commit 可用 側邊, 然後選勾勾 按鈕 V 來 Commit 也要加 註解
   - git push 可選 git -> ... -> push 或 sync (按最下面的圈圈也可以Sync = pull push 會 Merge )

   - Extensions 是左邊田字型按鈕 
    1. Remote  by Microdoft : 如果有Containder 用這個看 remote code
    2. Docker  by Microsoft : 可以用這個啓動 管理 Docker
    3. Github  by Github : 可以 Pull request. 其實不用裝也可以用 Git Hub. 在Terminal 設定好就好了
