# Basic

### 1. git status

현재 상태를 확인할 수 있다.

### 2. git add <파일 이름>

working directory의 파일을 staging area로 옮긴다.

```
git add a.js

git add *.js

git add *

git add .
```

### 3. git rm --cached <파일 이름>

staging area의 파일을 다시 working directory로 옮긴다.

### 4. git diff

파일의 변경된 내용을 알 수 있다.

### 5. git commit -m "<커밋 메세지>"

staging area의 파일을 commit 한다.

### 6. git commit -am "<커밋 메세지>"

working directory 와 staging area의 모든 파일을 commit 한다.

### 7. git log

깃 커밋 목록을 확인할 수 있다.

### 8. git tag <태그 이름>

커밋에 태그를 부여할 수 있다.

```
git tag v1.0.0

git tag v1.0.0 9186a41

git tag -d v1.0.0 // 태그 삭제
```
