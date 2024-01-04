# Github_study

## Git이란? ##

1. Git = 소스코드 및 파일 변경내역을 저장하는 분산 버전 관리 시스템
2. GitHub, Bitbucket, Gitlab 등의 Git 기반 버전 관리 호스팅 서비스들이 있다.

### Git과 Github 차이점 ###

1) Git
 * 로컬 저장소를 사용하기 때문에, 다른 사람들이 나의 작업 내용을 볼 수 없다.

2) Github
 * 개인의 로컬 서버 밖에서 Git 버전 프로젝트를 공유하고 기록하는 온라인 데이터 베이스.
 * 저장소를 깃허브에 제공해주는 클라우스 서버
 * 다른 사람들과 협업 시 소스코드 공유가 가능하며, 나의 작업 내용을 다른 사람들이 확인 가능하다.

<br> 

## Github 기본 용어 정리 ##

* Repository
  * 'rep' 또는 '저장소'라고 불리기도 한다
  * 프로젝트 저장 공간

* Local
  * 사용하고 있는 컴퓨터 혹은 노트북

* Remote
  * 원격 저장소

* Branch
  * rep 공간에서 독립적으로 작업을 하기 위한 공간
    
* Commit
  * 소스코드의 업데이트 확정. 확정이 될 경우 코드 상태를 메세지와 함께 Git rep에 저장
  * 로컬 저장소에는 변경이 반영되지만, 원격 저장소에는 아직 반영되지 않은 상태 ( push 필요)
    
* Pull
  * 원격저장소의 내용을 로컬저장소로 가져온다
    
* Push
  * Commit 내용을 원격저장소로 업로드
    
* CLI
  * `Command-line interface`의 줄임말
  * 명령어로 인터페이스 / 터미널을 통해 컴퓨터와 상호작용

* GUL
  * `Graphical User Interface`의 줄임말
  * 입출력 등의 기능을 아이콘 등의 그래픽으로 나타낸 것

<br> 

## Github 시작 ##

### 사용자 정보 등록 ###
`git config --global user.name "Your Name"`<br>
`git config --global user.email "you@example.com"`<br>

### git 상태 확인 방법 ###
​
`$ git log` // 모든 커밋 이력 확인<br>
`$ git log --oneline` // 모든 커밋에 대한 간단한 이력 확인<br>
`$ git log --oneline --graph` // 이력 그래프<br>
`$ git status` <- 현재 상태 확인<br>

### 로컬 저장 정보 삭제 ###

`git config --list` <- 정보확인<br>
`git config --unset --global user.name`<br>
`git config --unset --global user.email`<br>

### 디렉토리 명령어로 생성 ###

`$ mkdir 폴더명` // 저장소 생성<br>
폴더명과 폴더명 사이에 ^ 부호를 넣어 한번에 여러개의 폴더 생성 가능<br>


### 파일 명령어로 생성 ###

`$ touch 파일명` //  git에서 파일 생성<br>
폴더명과 폴더명 사이에 ^ 부호를 넣어 한번에 여러개의 폴더 생성 가능<br>

### 파일 등록 ###

`$ git add 파일명.확장자`<br>
`$ git add .` // 폴더 안 업로드가 필요한 모든 파일 등록. 간편해서 많이 사용된다 <br>


### 커밋 메세지 작성 ###

`$ git commit -m "작업내용 or 파일 설명"` // 구체적으로 작성, 커밋을 위해서는 필수 입력 필요<br>
`$ git commit -am "파일 설명"` // add, commit 동시에 설정 가능 (업로드가 되어있어야 사용가능)<br>



<br> 

## React 배포 ##
1. 배포하고자 하는 폴더에 cmd를 열어준다
2. `$npm i gh-page` 입력
3. package.json 폴더 name 위에 homepage 추가
4. package.json 폴더 scripts 쪽에 deploy 추가
   
```
   EX

  {
  "homepage": "https://xxxx.github.io/portfolio",  // 깃헙 페이지 주소 추가
  "deploy": "gh-pages -d build" // deploy 명령어 추가
}
```

5. `$ npm run build` 입력
6. Github rep 와 파일 연결 및 업로드 후 페이지 생성
7. `$ npm run depoly` 입력
8. github settings에서 pages gh-page로 변경






