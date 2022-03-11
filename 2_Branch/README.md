# Branch

### 1. git branch

현재 존재하는 브랜치를 확인할 수 있다.

```
git branch --all // 서버에 있는 브랜치까지 확인 가능
```

### 2. git branch <브랜치 이름>

브랜치를 생성한다.

### 3. git switch <브랜치 이름>

해당 브랜치로 이동한다.

### 4. git checkout <브랜치 이름> / <해시코드>

해당 브랜치 혹은 커밋으로 이동한다.

```
git checkout -b newbranch // 생성과 동시에 이동
```

### 5. git branch -d <브랜치 이름>

해당 브랜치를 제거한다.

### 6. git branch --move <기존 브랜치 이름> <바꿀 브랜치 이름>

브랜치의 이름을 변경한다.
