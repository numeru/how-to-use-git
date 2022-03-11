# Conflict

> 터미널에서 `git merge feature` 를 했을 때 충돌이 발생한 상황

### 1. 수동 해결

1. 충돌이 발생한 파일에서 원하는 부분만 남기고 모두 지운다.

2. `git add` 를 통해 수정한 파일을 커밋한다.

3. `git merge --continue` 를 통해 다시 merge 한다.

### 2. vscode로 해결

1. `git mergetool` 을 통해 vscode에 충돌이 발생한 파일을 연다.

2. 원하는 옵션 버튼 선택

   - Accept Current Change : 현재 있는 브랜치(HEAD)의 내용을 받아들인다.

   - Accept Incoming Change : merge 하려 했던 브랜치(feature)의 내용을 받아들인다.

   - Accept Both Change : 두 브랜치의 내용 모두 받아들인다.

   - Compare Change : 두 브랜치를 비교한다.

3. 파일을 저장하고 종료한다.

4. `git merge --continue` 를 통해 다시 merge 한다.

```
orig 파일이 생겼을 경우

1. `git config --global mergetool.keepBackup false`를 통해 설정을 끌 수 있다.

2. `git merge --abort` 를 통해 merge를 취소한다.

3. `git clean -fd` 로 orig 파일을 삭제한다.

4. 다시 merge 하고 위 방식으로 충돌을 해결한다.
```
