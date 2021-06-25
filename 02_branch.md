## branch command

- 브랜치 생성

```bash
$ git branch 브랜치명
```

- 브랜치 목록

```bash
$ git branch
```

- 브랜치 이동

```bash
# git checkout 까지만 입력한 상태에서 tab*2회 입력 => checkout 가능한 브랜치명 확인 가능
$ git checkout 브랜치명
브랜치명 $
```



```bash
$ git log --oneline
5ef6ea7 (HEAD -> master, origin/master, origin/HEAD) 210625 | git_repository modify
```

>  HEAD : 현재 우리가 속한 위치

```bash
$ git log --all --graph --oneline
# git의 모든 branch의 log를 그래프 형태로 표현
```

- 브랜치 생성+이동

```bash
$ git checkout -b 브랜치명
```

- 브랜치 병합

```bash 
(master) $ git merge 브랜치명
```

>  브랜치 병합 상태에서
>
> 1. i키 입력하여 수정상태 돌입
> 2. 수정 가능 상태에서 병합 커밋 메세지 수정 및 주석 삽입
> 3. esc로 수정상태 탈출
> 4. :wq 입력으로 병합완료

- 브랜치 삭제

```bash
$ git branch -d 브랜치명
```

- 브랜치 강제삭제

```bash
$ git branc -D 브랜치명
```

> merge 되지 않은 브랜치는 강제삭제해야함

## 3가지 병합 상황

### 1. fast forward

"다른 브랜치를 생성한 후, master 브랜치에 변경사항이 없을 때"

### 2. 3-way merge

"merge를 시행하는 현재 브랜치(master)가 지칭하는 커밋이 Merge할 브랜치의 조상이 아닐 때 git은 현재 브랜치와 머지할 브랜치의 커밋 2개와 두 브랜치의 공통조상 하나를 사용한다"

###### 1. 새로운 브랜치 signup 생성

###### 2. signup 브랜치에서 signup.py 생성

###### 3. master 브랜치에서 new folder 생성

##### 4. master 브랜치에서 signup 브랜치 병합

##### 5. signup 브랜치 삭제

### 3. Merge Conflict

"두 개의 브랜치가 동일한 위치의 파일을 수정 이후 merge를 시도할 때 발생하는 현상. 단, 동일한 파일을 수정했다 하더라도 서로 다른 영역을 수정하였다면 merge conflict는 발생하지 않는다."

- git 이 자동으로 병합하지 못하는 현상

##### 1. 새로운 브랜치 hotfix 생성

##### 2.  hotfix 브랜치에서 b.txt에 새로운 내용 입력

##### 3. master 브랜치에서 b.txt에 새로운 내용 입력

##### 4. master 브랜치와 hotfix 브랜치 병합

```bash
(master)$ git merge hotfix
Auto-merging b.txt
CONFLICT (content): Merge conflict in b.txt
Automatic merge failed; fix conflicts and then commit the result.

b.txt
<<<<<<< HEAD
master에서 수정했지롱
=======
hotfix 브랜치에서 수정내역 발생
>>>>>>> hotfix
```

- 수정사항 확인 및 정리 후 파일 add 및 commit 재실행





