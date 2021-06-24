# GIT 초기 설정

커밋 작성자 설정

````bash
# 명령을 시키고자 하는 주체
#git, 전역 설정 중애서 유저의 email을 설정 할거야.
$ git config --global user.email MiniePark1993@gmail.com
#git, 전역 설정 중에서 유저의 name을 설정 할거야.
$ git config --global user.name MiniePark
````

- 커밋을 작성하는 사람이 누구인지 알아야 하기 때문에

지정된 설정 확인

```bash
# git, 현재 전역에 설정된 설정 목록 보여줘
$ git config --global -l
# $ git config --global --list
```

# Git Basic

## 로컬 저장소 설정

```bash
$ git init 
```

- 폴더에 git 저장소를 초기화 하면,
  - .git 이라는 숨김 폴더가 생기고
  - bash에는 (master)라는 표기가 생성된다.

- 주의사항
  - .git 폴더를 직접적으로 수정하는 일은 없을 것이다.
  - 이미 git으로 관리하고 있는 (bash 창에 master가 표기 되어 있는) 폴더 내에서는 절대 git init명령어를 실행하지 말 것

# status

```bash
# git, 현재 관리중인 폴더의 상태 보여줘
$ git status
```

# add

```bash
$ git add 파일명 #git으로 관리하고자 하는 파일을 추가
$ git add directory_name # git으로 관리하고자 하는 폴더 내 모든 파일 추가
$ git add . # 현재 디렉토리 내 모든 파일 추가
```

- working directory 상태의 파일을 staging area 상태로 변경
- 커밋을 위한 파일 및 폴더들을 추가하는 명령어

# commit

```bash
#git, commit 할건데 -메세지는 "이걸로 해줘"
$ git commit -m "commit message"
# git commit -m "210624 | created CLI.md"
```

- 커밋을 통해 하나의 버전으로 기록 됨
- 커밋 메세지는 현재 변경사항들을 잘 나타낼 수 있도록 작성하는 것을 권장
- 커밋 목록은 `$ git log`를 통해서 확인 가능

```bash
$ git log # 커밋 내역 확인
$ git log --online # 커밋 내역을 한줄로 확인
```











