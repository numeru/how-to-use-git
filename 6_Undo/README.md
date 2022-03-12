# Undo

### 1. git restore <파일 이름>

파일의 변경 사항을 되돌린다.

```
git restore . // 모든 파일을 되돌린다.

git restore --staged file.txt // staging area에 있는 파일을 working directory 로 되돌린다.
```

### 2. git commit --amend

가장 최근 커밋을 수정한다.

```
git commit --amend -m "feature" // 가장 최근 커밋의 메세지를 수정한다.

git commit --amend // staging area의 파일을 가장 최근 커밋 안에 포함시킨다.
```

### 3. git reset <커밋 해시코드>

원하는 커밋으로 초기화한다.

```
git reset 3bd6f15 // 해당 커밋으로 되돌리고, 그 뒤에 커밋에서 수정한 사항들은 working directory에 남긴다.

git reset --soft 3bd6f15 // 해당 커밋으로 되돌리고, 그 뒤에 커밋에서 수정한 사항들은 staging area에 남긴다.

git reset --hard HEAD // 해당 커밋으로 되돌리고, 그 뒤에 커밋에서 수정한 사항들도 모두 삭제한다.
```

### 4. git reflog

모든 커밋 로그를 확인할 수 있다.
`git reset --hard` 로 초기화해도 로그에서 해시코드를 찾아 같은 명령어로 다시 이동할 수 있다.

### 5. git revert <커밋 해시코드>

해당 커밋에서 변경했던 모든 내용을 다 삭제해주는 커밋을 만든다.
이전 히스토리를 수정하지 않기 때문에, 서버에 이미 올라간 상황에 적합하다.

```
git revert --no-comit 0ddd7ab // 커밋을 만들지 않고 staging area에 되돌렸다는 사항을 남긴다.
```

### 6. git rebase -i <커밋 해시코드>

커밋 목록 중간에 있는 커밋 메세지를 수정할 수 있다.
해당 커밋 이후에 있는 모든 커밋들이 새로 만들어지는 것이기 때문에, 서버에 업로드 된 경우 주의해야한다.
명령어 옆에 적는 해시코드는 수정하고 싶은 커밋 바로 앞에 있는(이전의) 커밋의 해시코드 이다.
명령어 입력 후 원하는 옵션을 선택해준다. (reword: 커밋 메세지 변경, drop: 커밋 제거, edit: 커밋 수정)

---

### 1. 필요없는 커밋 삭제하기

1. git rebase -i <커밋 해시코드>
2. 해당 커밋 drop
3. git add .
4. git rebase --continue

### 2. 커밋 분리하기

1. git rebase -i <커밋 해시코드>
2. 해당 커밋 edit
3. git reset HEAD~1
4. 원하는 만큼 묶어서 모두 `git add`, `git commit -m ""`
5. git rebase --continue

### 3. 커밋 하나로 합치기

1. git rebase -i <커밋 해시코드>
2. 해당 커밋을 제외하고 하나로 묶을 커밋들을 squash
