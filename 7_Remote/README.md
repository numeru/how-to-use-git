# Remote

### 1. git remote

연결된 서버 정보를 가져온다.

```
git remote -v // 가리키는 곳을 확인할 수 있다.
```

### 2. git remote add <remote 이름> <링크>

서버를 추가로 연결한다.

### 3. git push

로컬의 커밋을 서버에 저장한다.

```
git push -f // local과 remote의 차이로 충돌이 발생했을 경우, local을 따르도록 한다.

git push origin feature // origin에 feature 브랜치를 저장한다.
```

### 4. git fetch / git pull

서버의 history를 받아오는 것은 같지만, fetch는 받아와도 로컬의 HEAD가 가리키는 곳은 변하지 않는다.  
반면 pull은 받아옴과 동시에 HEAD도 origin을 따라가게 된다.

```
git fetch

git fetch origin

git pull

git pull origin

git pull --rebase
```
