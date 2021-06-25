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



