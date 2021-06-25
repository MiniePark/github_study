# 원격 저장소 (remote repository)

## 기본 설정

1. 로컬 git 저장소 준비
2. github repository 생성
3. Repository default branch 변경

# 명령어

## 원격 저장소 주소 추가

```bash
# git, 원격 저장소 주소를 origin 이라는 이름으로 추가하고, 해당하는 주소는 다음과 같아.
$ git remote add origin https://github.com/MiniePark/github_study.git
# $ git remote add 저장소명 주소
```

# 원격 저장소 목록 보기

```bash
$ git remote -v
```

### 원격 저장소 삭제

```bash
$ git remote rm origin
# $ git remote rm 저장소명
```

### 원격 저장소에 업로드(push)

```bash
# git, origin이라는 명칭의 원격 저장소에 master 브랜치의 commit 내역들을 업로드해줘.
$ git push -u origin master
```

- commit 내역이 없으면 업로드 불가능

### 원격 저장소로부터 복사(clone)

```bash
# git, repository의 모든 내용들을 로컬 드라이브에 복사해와줘
$ git clone [주소]
# git clone https://github.com/MiniePark/github_study
```

- 이미 git init이 되었음을 숙지

### 원격 저장소로부터 변경사항 업데이트(pull)

```bash
# git, repository의 변경 사항을 로컬 드라이브에 업데이트 해줘
$ git pull [저장소명] [branch]
# git pull origin master
```

