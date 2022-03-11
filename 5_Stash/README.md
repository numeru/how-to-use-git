# Stash

수정한 파일을 commit 하지 않고 저장해두고 싶은 경우 (다른 브랜치로 전환해야 하는 경우 등)  
stash를 이용할 수 있다.

### 1. git stash

파일을 stash로 저장한다.

```
git stash

git stash push

git stash push -m "feature A" // working directory 와 staging area에 있는 모든 파일을 stash로 저장한다.

git stash push -m "feature B" --keep-index // staging area 에 그대로 둔 채 stash로 저장한다.

git stash -u // untracked 파일까지 stash로 저장한다.
```

### 2. git stash list

stash 목록을 확인할 수 있다.

### 3. git stash show <stash ID>

해당 stash의 내용을 확인한다.

```
git stash show stash@{4}
```

### 4. git stash apply

stash를 목록에 그대로 유지하면서 적용한다.

```
git stash apply // 가장 최근 stash를 적용한다.

git stash apply stash@{3} // 해당 stash를 적용한다.
```

### 5. git stash pop

stash를 목록에서 제거한 뒤, 적용한다.

### 6. git stash drop <Stash ID>

해당 stash를 목록에서 제거한다.

### 7. git stash clear

모든 stash를 제거한다.

### 8. git stash branch <브랜치 이름>

새 브랜치를 생성하고 가장 최근 stash를 가져온다.
