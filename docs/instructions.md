# Git 常用指令整理

整理常用 Git 指令，附上全稱、說明與簡單範例，便於快速查閱與記憶。

---

## 初始化與基本操作

| 指令 | 全稱 | 說明 | 範例 |
|------|------|------|------|
| `git init` | initialize | 初始化一個 Git 倉庫 | `git init` |
| `git status` | status | 查看目前檔案狀態 | `git status` |
| `git add .` | add | 將所有檔案加入暫存區（一點表示所有檔案） | `git add .` |
| `git commit -m "訊息"` | commit (message) | 提交一次變更，附上訊息 | `git commit -m "init"` |
| `git log` | log | 顯示提交紀錄 | `git log` |
| `git diff` | difference | 顯示變更差異 | `git diff` |

---

## 遠端操作 Remote

| 指令 | 說明 | 範例 |
|------|------|------|
| `git remote add origin [url]` | 新增遠端 repo 並命名為 origin | `git remote add origin https://github.com/user/repo.git` |
| `git push -u origin main` | 推送並設定追蹤主分支 | `-u` 是 `--set-upstream` 的縮寫 | `git push -u origin main` |
| `git pull` | 拉取遠端最新變更 | `git pull` |
| `git clone [url]` | 複製整個遠端 repo 到本地 | `git clone https://github.com/user/repo.git` |

---

## 分支操作 Branch

| 指令 | 說明 | 範例 |
|------|------|------|
| `git branch` | 查看目前所有分支 | `git branch` |
| `git branch [name]` | 建立新分支 | `git branch dev` |
| `git checkout [name]` | 切換到指定分支 | `git checkout dev` |
| `git switch [name]` | 切換分支（較新語法） | `git switch dev` |
| `git merge [name]` | 將某分支合併進目前分支 | `git merge dev` |
| `git branch -d [name]` | 刪除分支（若已合併） | `git branch -d dev` |

---

## 歷史操作與修正

| 指令 | 全稱 | 說明 | 範例 |
|------|------|------|------|
| `git reset` | reset | 回到指定狀態（危險） | `git reset --hard HEAD~1` |
| `git revert` | revert | 反向提交，保留歷史 | `git revert abc1234` |
| `git stash` | stash | 暫存變更，方便切分支 | `git stash` |
| `git rebase` | rebase | 重整提交歷史 | `git rebase main` |

---

## 檔案管理

| 指令 | 全稱 | 說明 | 範例 |
|------|------|------|------|
| `git rm [檔案]` | remove | 從 Git 中刪除檔案 | `git rm test.txt` |
| `git mv 舊名 新名` | move | 改名或搬移檔案 | `git mv old.txt new.txt` |

---

## 設定與工具

| 指令 | 全稱 | 說明 | 範例 |
|------|------|------|------|
| `git config --global user.name` | configuration | 設定使用者名稱 | `git config --global user.name "frog"` |
| `git config --global user.email` | configuration | 設定使用者 email | `git config --global user.email "frog@mail.com"` |
| `git config --list` | configuration | 顯示所有 git 設定 | `git config --list` |

---

## 認證與憑證

| 指令 / 概念 | 說明 |
|-------------|------|
| Personal Access Token (PAT) | 取代 GitHub 密碼進行 HTTPS 認證 |
| SSH 金鑰 | 以公開金鑰方式認證 GitHub 推送操作 |
| `.gitignore` | 指定哪些檔案不要被 Git 管理（例如 log、venv、node_modules 等） |

---

## 備註縮寫說明一覽

| 縮寫 | 全稱 | 意義 |
|------|------|------|
| `-m` | message | 提交訊息內容 |
| `-u` | upstream | 設定追蹤遠端分支 |
| `-d` | delete | 刪除（分支） |
| `-f` | force | 強制執行 |
| `-v` | verbose | 顯示詳細資訊 |
| `-M` | move | 強制重新命名分支 |

---

> 筆記由 YAN CHENG-YU 整理，如有錯誤歡迎指正或討論。
