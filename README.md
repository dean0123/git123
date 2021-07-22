# 1. 什麼是 git?  
  - 5W1H, 每樣東西都要先問 5W1H, 人事時地4w, 前因(Why)後果(How)
  - what 事: 什麼是git? 
  - who 人: 
  - when 時:
  - where 地:
  - why 因:
  - how 果:  

![git](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d8/Git_operations.svg/588px-Git_operations.svg.png) 


# 2. 什麼是 github?  跟 git 一樣嗎? 
- git 是一種**版本控制**的東西, 等於是**存檔**的概念, 
  - 就好象玩 game 可以存檔, 下次繼續玩一樣.  git 還可以存很多次, 就好象玩 game 可以在第三關存一次, 第五關存一次, 之後每關都會存, 等到打到第八關的時候, 發現其實第六關就走錯了, 這個時候, 就可以把第五關叫出來, 從第五關開始打. 
  - git 也是一樣, 寫程式每次**改完了一版**, 測試完了以後, 都要**養成好習慣 用 git 存起來**. 以免殺錯了檔案  或改錯了 從的 , 都可以從之前的某個存檔的版本叫出來.  所以要養成好的習慣, 在一開始寫 code 或是其他文件的時候, 就先設定用 git 來做版本控制與存檔. 
  - git 還有特異功能, 讓多人一起玩, 就像兩人一組一起闖關, 有人得到3個寶石存檔, 另外的人得到5個子彈存檔, 這樣你們一起的進度就會有3個寶石與5個子彈, git 也可以人讓多人一起開發code, 然後把之後多人修改的從的 code, merge 組合成一個共同的 code. 這個以後再慢慢了解. 
  
- github 是把 git code 存放在雲端的一個服務. 
  - git 本來是把 code 是放在本機自己用, 但是去了學校公司, 換了電腦, 換了地方, 就拿不到code, 也不能多人共用一起開發.  
  - github 是一個**雲端網頁的 git 服務**, 想像成 git 雲端的 hub, 透過 git 可以把本機的 code 指定放到雲端的 github 裏面, 這樣走到哪裏就都可以繼續 code 的開發, 也可以多人共用. 也不怕換電腦了. 除了 github, 還有很多其他的 git 雲端服務, 像是 gitlab, heroku 等等
  - github 除了放 code, 還可以把相關的專案, 文件, 說明, 網頁都放在這裏, 像是這一片文章就是 github 的一個說明檔 README.md 作出的靜態網頁. 


# 3. 安裝 git
- git 需要安裝, `google git` 找到就可以**下載 git 安裝**了, 很快很小, 裝好後重開`Terminal` 下指令測試一下
```javascript
$ git --version      (有版本號碼出來就對了) 
```
- github **不用安裝**, `google github` 找到 github 網頁去申請一個帳號密碼, 然後就可以使用了, 可以
  1. 登入後, 建立一個 **repository (儲存位置)** , 先叫做 **test123** 好了, 用來裝你的程式
  2. 按 綠色的 `code` 按鈕, 會看到 repository 的 http 連結. 複製一下等下 git 要用來 設定 remote 的存放點. 

# 4. 使用 git add commit 到本地資料庫
- 簡單試用看看 git init, add, commit, checkout
```javascript
$ cd dir01                 (cd到工作目錄， 一般每個工作目錄, Project 都要單獨設定一次, )
$ git init                 (把這個目錄 git init 初始化 )
$ git status               (常常都要用 git status 看狀態)
$ git add .                (把檔案加到 git stage 暫存的 stage) 
$ git commit -m "mesg.."   (把 暫存 stage 裏面的檔案 確認 commit 到本地暫存 目前 Branch 分支）
                           -m 是 確認這個版本的 message 訊息, 方便日後查詢
                           -a 是 commit 時， 也 add 加入新的檔案
$ git log                  (列出 user time commit message 跟 內容）                           
$ git reflog               (列出 commit 內容）                           
$ git branch -a            (查現在的分支 branch 是什麼，本機預設是 master， github 預設是 origin main， heroku 是 heroku main ）                           
$ git checkout -b xxxx     (切換 branch 分支， 可切換到副分支， 也可切換回主分支 master， 將檔案叫回來 到工作目錄中）
$ git merge                (合併 branch 分支， 一般是切換 checkout master 到主分支， 然後再合併 某一個 副分支 ）
  
$ git config --list                                 (list config ）
$ git config --global user.name "Dean"              (set user name）
$ git config --global user.email "Dean@gmail.com"   (set user email）
```  
# 5. 用 git push 到遠端/雲端資料庫
- **遠端**資料庫一般是 `git server` ， 公司內部 或 團體開發用的。 
- **雲端**資料庫如 `github`
```javascript
$ git remote add origin https://github.com/你的帳號名稱/test123.git  (<-- 貼上剛剛複製的連結)
                          (設定 git 目錄 code 放到 github, 不行就先 git remote rm origin)
$ git remote -v           (查看 git remote 是哪一個 repository） 
$ git branch -M main      (設定 code 主要分支爲 main)
$ git push -u origin main (把 code 推送到雲端 github, 之後就 只要 $git push 就好)
$ git pull                (把 code 從雲端 GitHub 拉下來 )
```  




# 6. git 說完了， 現在換 github 了。 把 github 的 repository 變成一個網頁
- 如何把 各自的 github repository 變成各自單獨網頁
- github 裏面 選 repositoty 後, 選 settings 設定, 左邊下面有個 pages 點開, 
- 然後 source 選 `main` -> 目錄 選 `/root` -> theme 隨便選一個， github 會把 `README.md` 會自動轉爲網頁， 你可以回去修改內容  
- 比方說 github 帳號是 `dean0123`, 剛剛加的 repository 叫做 `node123` 那麼 新網頁就是  [`https://dean0123.github.io/node123`](https://dean0123.github.io/node123)  
有時候會等一分鐘才更新

# 7. 如果你把 github Repository 跟你 的 **github帳號** 有關， 會有特別的功能
- 第一個 就是 把 repository 設成剛好跟你的 **github 帳號** 一樣    
例如我的 `dean0123`， 那麼 github 會把它變成我的 github 的主頁 [`https://github.com/dean0123`](https://github.com/dean0123) 
- 另一個是 把 repository 設成你的 **github 帳號** 後面加 `github.io`   
例如我把 Reposotory 設成 `dean0123.github.io` 這個帳號的網址會直接變成獨立的 [`https://dean0123.github.io`](https://dean0123.github.io)  酷吧 

# 9. VSCode 上也可以用 git， 按 V 勾勾按鈕， 再按 下面等圈圈 Sync (另外開Repository pages)
1. 安裝使用, 到 cd 工作目錄 下 打
```javascript
$ code .
```

2. 安裝 相關的 外掛 (git, github, docker 等...)
   - git commit 可用 側邊, 然後選勾勾 按鈕 V 來 Commit 也要加 註解
   - git push 可選 git -> ... -> push 或 sync (按最下面的圈圈也可以Sync = pull push 會 Merge )

   - Extensions 是左邊田字型按鈕 
    1. Remote  by Microdoft : 如果有Containder 用這個看 remote code
    2. Docker  by Microsoft : 可以用這個啓動 管理 Docker
    3. Github  by Github : 可以 Pull request. 其實不用裝也可以用 Git Hub. 在Terminal 設定好就好了
