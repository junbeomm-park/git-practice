## GIT 협업



### 협업 하기

A = 로컬 저장소 1

B = 로컬 저장소 2

C = Github (원격저장소)



##### 1. A는 프로젝트 파일을 Github에 올린다

1. A는 Github에 repository를 생성 하여 B를 collaborator 로 추가한다

* collaborator로 추가해야 B가 해당 프로젝트에 **pull** , **push** 할 권한이 생긴다



2. A는 각종 기본 라이브러리들을 추가해서 초기 프로젝트를 셋팅



3. 셋팅을 마쳤으면 B 가 프로젝트 파일 받을 수 있도록 Github에 push

```
$ git init
$ git add .
$ git commit -m "프로젝트"
$ git remote add origin 주소
$ git push origin master
```



##### 2. B는 프로젝트 파일을 자신의 PC로 가져온다.



1. B는 A가 작업한 파일을 **clone** 해서 가져온다

2. **git clone** 을 하면 자동으로 원격 저장소(remote repository)가 등록된다.

```
$ git clone 주소
```



##### 3. A,B는 각각 브랜치를 생성하여 작업을 진행

1) A,B는 각각 자신의 PC에서 brchA,brchB 이름의 **branch** 를 생성해서 독립된 작업 공간을 마련

``` 
$ git branch brchA
$ git branch brchB
```



2. 이제 A,B는 Github를 공유하고 있는 상황이며, 독립적인 지역 저장소를 갖고 있다.
3.  A, B는 각자 구현할 기능이 정해져 있고 , 각 기능을 끝낼 때 마다 Github에 자신의 작업물을 **push** 한다.
4. 병합이 필요할 때 master 브랜치에 **merge** 를 한다.



##### 4. B 가 작업을 마치고 master branch에 병합

```
$ git add .
$ git commit -m "프로젝트2"

$ git checkout master
$ git merge brchB
$ git push origin master     
```

1. B는 master 브랜치에 push 하기 전에 , 자신의 지역 저장소에 있는 master 브랜치에 brchB 브랜치를 **merge** 한다.
2. 그리고 local master 브랜치에서 Github master 브랜치로 push



#### 5. A는 작업 중 B가 올린 최신 작업물을 갖고 와서 작업을 진행

1. A는 B가 push한 최신 작업물을 사용하기 위해 Github에서 master 브랜치를 **pull** 한다.
2. A는 pull 할때 master 브랜치로 이동한 후, pull 한다
3. 브랜치를 이동할 때, 작업을 마무리하고 commit을 한 후 이동해야 한다

```
$ git checkout master

$ git pull origin master

```

4. 최신 작업물을 가져 왔으면, 자신의 작업본에 반영해야 한다.
5. brchA 브랜치로 이동 후 master 브랜치를 **merge** 

```
$ git checkout brchA

$ git merge master
```

