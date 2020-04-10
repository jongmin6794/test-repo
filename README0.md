# Git

> Git은 분산버전 관리 시스템(DVCS)중 하나이다.

# Git 기초 흐름

### 0. 저장소 설정

```bash
$ git init #```bash
```

깃 저장소를 만들게 되면 해당 디렉토리 내에 

### 1.  `add`

```bash
# 
$ git status

# 트래킹 되고 있지 않은 파일들
# => git으로 버전으 남긴적이 없는 파일

# 커밋 될(will be committed)
# staging area에 포함시키려면, git add
# (커밋될 파일 목록)
# 커밋할 내용 없지만, 트래킹 되지 않는 파일은 존재한다.
# => WD O, Staging Area X
```

staging area에 추가

```bash
$ git add a.txt     # a.txt 파일
$ git add myfolder/ # myfolder 폴더
$ git add .         # 현재 디렉토리
```

추가 후 상태

```bash
$ git status
# 커밋될 변경사항들(staging area)
# a.txt 새로 생성됨
```

### 2. commit

커밋 메시지는 현재 버전에 대해 명확하게 작성

```bash
$ git commit -m '커밋메시지'
```

- 커밋 이력을 확인하기 위해서는 아래의 명령어를 입력한다.

```bash
$ git log
$ git log -1 # 최근 한개 커밋
$ git log --oneline # 간략한 로그
$ git log --oneline -1 # 최근 한개의 커밋을 간략하게
```

* 원격 저장소 설정

  ```bash
  $ git remote add origin {_url__}
  ```

  * 원격저장소(remote)로 origin 이름으로 url을 추가(add)

* 원격 저장소 목록

  ```bash
  $git remote rm origin
  ```

  

* 원격 저장소 삭제

```bash
$ git push origin master
```

* 현재 폴더를 그대로 업로드 하는 것이 아니라, 지금까지의 이력/ 버전을(commit)을 push하는 것이다.
* working directory, staging area 의 변경사항들은 원격저장소로 push 되지 않는다
* 따라서, push 전에 $ git staus, $ git log 를 통해서 확인하는 습관을 가지자

### 2. pull

```bash
$ git pull origin master
```

* 원격저장소 변경 사항(이력)을 받아온다.

