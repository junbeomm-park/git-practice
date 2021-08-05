## 버전관리의 시작







### 저장소(repository) 만들기

> 저장소를 만들고 싶은 디렉터리로 이동해서 깃을 초기화하면, 그때부터 해당 디렉터리에 있는 파일들을 버전 관리 할 수 있다.





#### 깃 초기화화기 - git init



##### 1) 깃 저장소를 만들 디렉터리를 하나 새로 만든 후, 새로만든 디렉터리로 이동

* 홈 디렉터리에 hello-git 이라는 디렉터리를 만든다.
* cd 명령을 이용해 hello-git 디렉터리로 이동.

```
$mkdir hello-git
$cd hello-git
```

##### 2) hello-git 디렉터리에 저장소를 만들기 위해 git init 명령을 입력한다 . 

* git init 명령은 깃을 사용할 수 있도록 디렉터리를 초기화
* init은 (initialize)의 약자

```
$git init . 
```





## 버전 생성





### 깃 (Git) : 버전 관리 시스템

> 쉽게 버전을 만들고, 만든 시간과 수정 내용까지 기록할 수 있는 것이 버전 관리 시스템
>
> > 원래 파일 이름은 그대로 유지하면서, 변경 시점마다 저장
> >
> > > 각 버전마다 작업했던 내용을 확인할 수 있고, 그 버전으로 되돌아갈수 있음



#### 작업 트리(working tree) / 작업 디렉터리(working directory)

* 작업 트리는 파일 수정, 저장 등의 작업을 하는 디렉터리
* 작업 트리(working tree)는 작업 디렉터리(working directory) 라고도 한다.
* 'hello-git' 디렉터리가 작업 트리



####  스테이지(stage) / 스테이징 영역(staging area)

* 스테이지는 버전으로 만들 파일이 대기하는 곳
* 스테이지(stage)는 스테이징 영역 이라고도 부른다.
* 눈에 보이지 않음
* 깃을 초기화했을 때 만들어지는 .git 디렉터리 안에 숨은 파일 형태로 존재



#### 저장소(repository)

* 저장소는 스테이지에서 대기하고 있던 파일들을 버전으로 만들어 저장하는 곳
* 눈에 보이지 않음
* 깃을 초기화했을 때 만들어지는 .git 디렉터리 안에 숨은 파일 형태로 존재



####  명령어 및 용어



`git status` : 깃의 상태

`commits` : = virson

`Untracked` : 추적 되고 있지 않은

`git add hello1.txt`  : hello1.txt 파일을 staging area에 올릴때

` git commit -m "파일명" ` : git 에게 버전 만드는 명령어

`git log` : 버전이 잘 만들어 졌는지 확인





#### hello1.txt 파일 버전 만들기



`nano hello1.txt`

`cat hello1.txt` 

` git status` - 상태확인

`git add hello1.txt`

`git commit -m "hello1.txt"` 

`git status` - 상태 다시 확인

`git log` 





## 버전간의 차이점 비교

 



### git diff : 변경 사항 확인하기

> 스테이지에 있는 파일과 저장소에 있는 최신 커밋을 비교해서 수정한 파일을 최종 검토





`git diff` : 버전의 차이점

`git log -p`  : 버전과 버전 파일과 파일을 비교





## checkout



`git chekout` : 저장소를 버전을 만드는 시점으로 되돌리기, 이를 통해서 버전과 버전을 넘나 들수 있다.





## 버전 삭제 - git reset





`gir reset` : xx 버전으로 리셋 하겠다.





## 버전 되돌리기 - git revert



`git revert` : 버전을 삭제하지 않으면서, 되돌리는 방법





























 

















