# CLI(Command Line Interface)

## ls

- `-`은 앞에 목록 형태를 나타낼 수 있다.
- ls 명령어는 현재 작업중인 위치에 존재하는 파일 혹은 폴더 목록을 보여준다
- `백틱 3개는 코드 블락을 생성 할 수 있다.

``` bash
Minie@DESKTOP-JGSDPD9 MINGW64 ~/Desktop/Github_study
$ ls
'test folder'/   test.txt
```

## cd (change directory)

- 현재 작업중인 디렉토리(a.k.a 폴더)를 변경하겠다.
- git bash에서 입력 중 탭(Tab) 입력 시 자동완성

```bash
Minie@DESKTOP-JGSDPD9 MINGW64 ~
> cd {directory name}
$ cd desktop/github_study
Minie@DESKTOP-JGSDPD9 MINGW64 ~/Desktop/Github_study
$ cd .. # 내 상위 폴더로 이동
```

## mkdir (make directory)

- 디렉토리/폴더를 생성한다.

``` bash
Minie@DESKTOP-JGSDPD9 MINGW64 ~/Desktop/Github_study
$ mkdir {directory name}
```

## touch

- 파일을 생성한다

```bash
Minie@DESKTOP-JGSDPD9 MINGW64 ~/Desktop/Github_study
$ touch {filename}.{확장자}
```

