>
>
>'>'꺽쇠 인용문



# git 기초문법

>git은 분산형 버전관리시스템(DVCS)이다.



#GIT 사전준비

1. 윈도우 > [GIT bash](https://gitforwindows.org/)를 설치한다
2. 로컬설정

```bash
$ git config --global user.name 'thtm111'
$ git config --global user.email 'thtm11111@gmail.com'
```

*  처음 git을 설치하면, commit을 하는 작성자(author)를 설정해야한다
* email 정보는 github에 등록된 이메일을 설정하는 것을 추천
* 설정된 내용을 확인하기 위해서는 아래의 명령어를 입력한다.

```bash
$ git config --global -l (엘)
user.name=thtm111
user.email=thtm11111@gmail.com
```

* ​	오프라인 강의장에서 하는경우 반드시 체크



기초흐름

> 작업 > add  > commit
>
> 작업이 끝나면, 커밋할 파일을 모아서 (add), 커밋한다(버전을기록한다.)



# 0.저장소 설정

```bash
$ git init
Initialized empty Git repository in C:/Users/changdo/Desktop/정리/.git/

$ (master)

```

* git 저장소로 활용하기 위해서는 위의 명령어를 활용한다.
  * `.git` 폴더가 생성
  * `master`로 현재 작업중인 브랜치 확인

# 1.add

> 커밋을 위한 파일목록(staging area)

```bash
$ touch test.txt
```

* add 전 모습

```bash
$ git status

On branch master

No commits yet
# 트래킹이 되지 않는 파일 : WD O

Untracked files:
	#GIT add 명령어를 사용!
	#커밋이 될 것에 포함시키기 위하여..
  (use "git add <file>..." to include in what will be committed)
        test.txt
# 맨 마지막 줄 : 총정리
#noting added to commit / 커밋하기 위해 추가된 것 X : stagin area X
#untracked files present : WD O
nothing added to commit but untracked files present (use "git add" to track)

```



* add후의 모습

```bash
$ git add .
$ git status
On branch master

On branch master

No commits yet
# 커밋이 될 변경사항 : SA O
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        # 새 파일 : test.txt
		new file:   test.txt


```

# 2.commit

> 버전을 기록(스냅샷)

```bash
$ git commit -m '커밋 메시지'
[master (root-commit) db0cb2c] 커밋 메시지
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt


```

* 커밋 메시지는 현재 작업의 내용을 알 수 있도록 명확하게 작성한다
* 커밋 이력을 확이하기 ㅜ이해서는 아래의 명력어를 활용한다.

```bash
$ git log
commit db0cb2caa3b4c4fe8bbc649b959c5f2853d28af0 (HEAD -> master)
Author: thtm111 <thtm11111@gmail.com>
Date:   Tue Dec 22 14:37:22 2020 +0900
    커밋 메시지

```

* 추가옵션

  ```bash
  $ git log -l
  $ git log --oneline
  db0cb2c (HEAD -> master) 커밋 메시지
  $ git log --oneline -l
  ```

  

# 상태확인

> git 저장소의 현재상태는 status로 확인하는 습관을 기르자

```bash
$ git status
```

