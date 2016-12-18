# 回顧一下上一節課...
## 要把程式碼回覆到上一個版本的狀態...
```
git reset --soft HEAD^
git reset --hard HEAD^
git commit --amend
```

## 若要檢查現在工作目錄的狀態：
```
git status
git log
```
## 若要檢查尚未 commit 的程式碼與上個版本的差別：

```
git diff
git diff --cached
```
## branch 等於程式碼的平行世界，一個 branch 上的程式碼不會影響到另一個 branch 的程式碼 ：
```
git branch 新分支名稱
git checkout 我要切換到的分支名稱
```
## 查看儲存庫目前的樹狀圖
```
git log --oneline --graph --all
```

# 合併分支
今天一你不管在一個分支上做了多少開發，終究還是需要把該分支和預設分支 (master) 進行合併，這樣才會把分支上的 commit 納入 master 裡面  

## 前置作業
```
mkdir lesson3

git init

echo '# hello world!' >> lesson3_1.md

git add lesson3_1.md

git commit -m "added lesson3_1.md"

echo '# hello world!' >> lesson3_2.md

git add lesson3_2.md

git commit -m "added lesson3_2.md"

git branch feature

git checkout feature
```

### 現在我們在 feature branch 上做一個 commit...
```
echo '# another hello world!' >> lesson3_1.md

git add lesson3_1.md

git commit -m "edit lesson3_1.md"
```

### 現在我們就回到 master branch 上：
我們再用 git log 看一下，此時的 master 應該只有兩個 commit

### 接下來把 feature branch 上面的 commit 合併到 master branch 上：
```
git merge feature
```
用 git log 查看一下，此時 feature branch 上面的 commit 已經被成功合併入 master 裡面了

### 接下我們再開出另一個 feature branch:
```
git branch faeture2
git checkout feature2
```

### 接下來在我們的 feature branch 上對 lesson3_2.md 進行修改並且 commit
```
echo '# this is my second line of code' >> lesson3_2.md

git add lesson3_2.md

git commit -m "edited lesson3_2.md"
```
## 接下我們回到 master branch 上:
```
git checkout master
```
## 接下來在我們的 master branch 上對 lesson3_2.md 進行修改並且 commit
```
echo '# this is my second line of code on master branch' >> lesson3_2.md

git add lesson3_2.md

git commit -m "edited lesson3_2.md on master"
```

## 此時我們若執行 git merge feature2...
```
git merge feature2
```

## 面對 conflict，我們能做的事就是手動把衝突的地方修好並做 commit
```
# hello world!
<<<<<<< HEAD
# this is my second line of code on master branch
=======
# this is my second line of code
>>>>>>> feature2


從 <<<<<<< HEAD 到 ======= 的內容，HEAD 代表當前 master 分支的最新版 lesson3_2.md 內容

從 ======= 到 >>>>>>> feature2 的內容，代表 feature2 分支裡的 lesson3_2.md 內容
```
