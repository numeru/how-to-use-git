# Merge

### Rebase로 merge하기

> master 브랜치에 feature 브랜치를 병합하는 상황

merge commit이 발생하는 three-way merge가 싫다면 rebase를 통해 fast-forward merge를 할 수 있다.
내용만 같은 새로운 commit을 만드는 것이기 때문에, 같은 브랜치에 다른 개발자가 작업하고 있거나 이미 서버에 올라가 있다면 피하는 것이 좋다.

1. `git checkout feature` 를 통해 병합 할 브랜치로 이동한다.

2. `git rebase master` 를 통해 rebase를 적용한다.

3. `git checkout master` 를 통해 다시 돌아온다.

4. `git merge feature` 를 통해 merge 한다.
