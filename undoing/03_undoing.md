## undoing

> 원상태로 되돌리기

#### 1. 폴더 undoing 생성

#### 2. undoing 폴더 안으로 작업위치 변경

#### 3. un.txt, doing.txt 파일 생성

### 1. 파일 상태를 unstage로 변경하기

#### 첫번째

```bash
$ git rm --cached (파일명)
# 파일을 add되지 않은 unstage 상태로 변경한다.
```

- 따로따로 커밋하려 했는데 실수로 전부 $ git add . 해버렸을 때
- 혹은 최초로 add를 한 상황(해당 파일들에 대한 commit이 없을 때)

#### 두번째

#### 1. un.txt, doing.txt 파일 둘 다 커밋 남기기

#### 2. 두 파일 모두 수정사항 남기기

#### 3. git add . 하기

```bash
$ git restore --staged (파일명) #un.txt
```

## 2. Modified 파일 되돌리기

- commit 기록은 남아있고, 새롭게 수정한 다음 아직 add 하지 않은 working directory에 존재하는 파일의 수정사항을 되돌린다.

```bash
$ git restore {파일명}
# modified 된 파일을 commit 기록된 상황으로 되돌린다.
```

- 주의사항
- 수정한 내역 전부를 과거를 되돌리는 것이기 때문에 수정한 내용 전부가 사라진다.
- 절대 복원 불가능
- 진짜진짜 수정한 내용이 마음에 안 들 때만 쓴다.

## 3-1 Commit Messege 수정

> 마지막으로 커밋하고 나서 수정한 게 없는 상황일 때(커밋 하자마자 명령을 시행할 떄)
>
> 커밋 메세지만 수령

```bash
$ git commit --amend
```

1. vim 진입
2. 키보드 `i` 혹은 `insert` 키 입력
   - --insert--상태로 전환
3. 수정하고자 하는 commit messege 입력
4. `Esc` 키 입력
   - --insert--상태 탈출
5. :wq 입력 (write quit)

#### ※bash 창 기준 커서 앞 내용 전부 지우기 `Ctrl+u` 

## 3-2 커밋할 때 파일을 빼먹었다면...

```bash
$ touch foo.txt bar.txt
$ git add foo.txt
$ git commit -m "foo&bar"

#실수로 bar.txt를 빼먹고 commit 한 다음에...
$ git add bar.txt
$ git commit --amend

$ got log --oneline
38dbc63 (HEAD -> master) foo&bar
# 새 커밋을 만드는 게 아니라
# 가장 최신의 커밋을 재작성 하는 것
```







