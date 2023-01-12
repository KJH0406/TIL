# TIL

# 교육자료

- CLI란

= 명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식.

- GUI : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식

GIT CLI기능

bash : CLI 프로그램

ls : 목록 확인

clear : 지우기

mkdir : make directory, 디렉토리 만들기 **mkdir 폴더명 (ex. mkdir blackpink)**

cd : change directory, 디렉토리 이동

cd 위치(**(ex. cd blackpink)**

cd .. : 상위 폴더로 이동 (띄어쓰기 주의)

pwd : print working directory, 현재 나의 디렉토리 위치를 알려줌.

**cd 누르고 영어 몇개 쓴다음에 탭키 누르면 뒤에꺼 자동완성**

- find -name 파일명 하면 한번에 찾을 수 있음

rmdir : remove directory , 파일 삭제하는 기능

     rmdir 폴더명

rmdir **test** 라고 명령어를 날렸고, 삭제되지 않았다.

rmdir: failed to remove `**test**': Directory not empty

이유(Directory not empty)는 해당 폴더가 비어있지 않아서 문구가 떴다.

강제로 해당 폴더와 내부 파일을 삭제할려면 다음과 같은 명령어를 사용하면 된다.

rm -rf **test**

만약, 권한거부가 되면 sudo rm -rf **test** 로 실행하자

옵션 :

- r : 삭제시 하위 경로 모든 파일과 폴더 삭제 (recursive)
- f : 안 물어보고 삭제(force)

**vs코드 단축키(shortcut)**

[[VSCode] 💽 유용한 단축키 모음 - 개발을 누구보다 빠르게](https://inpa.tistory.com/entry/VS-Code-%E2%8F%B1%EF%B8%8F-%EC%9C%A0%EC%9A%A9%ED%95%9C-%EB%8B%A8%EC%B6%95%ED%82%A4-%EC%A0%95%EB%A6%AC)

 `ctrl + `(backtick, 백틱)` 를 통해 터미널을 열고 닫을 수 있음

## **Markdown(마크다운)**

[Markdown Cheat Sheet | Markdown Guide](https://www.markdownguide.org/cheat-sheet/)

[마크다운(Markdown) 사용법](https://gist.github.com/ihoneymon/652be052a0727ad59601)

[마크다운 왕초보 코드블록 사용가능한 언어 목록(초간단)](https://velog.io/@cateto/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4-%EC%99%95%EC%B4%88%EB%B3%B4-%EC%BD%94%EB%93%9C%EB%B8%94%EB%A1%9D-%EC%82%AC%EC%9A%A9%EA%B0%80%EB%8A%A5%ED%95%9C-%EC%96%B8%EC%96%B4-%EB%AA%A9%EB%A1%9D%EC%B4%88%EA%B0%84%EB%8B%A8)

- git hub 에서 보는 readme.md가 마크다운 파일임.
- 마크업이란? , 태그(Tag)를 이용하여 문서의 구조를 나타내는 것.
    
    마크다운 파일의 파일명은 .md 임.
    
- 코드 입력 후 preview를 클릭하면 실행된 결과를 볼 수 있음.
- [string](url) or ![string](img_url) 하면 링크던 이미지던 링크걸 수 있음 스트링이 보이는 부분임
- **텍스트**(강조)

# Git이란?

1. Repository
    1. 특정 디렉토리를 버전 관리하는 저장소
        1. git init 명령어로 로컬 저장소를 생성.
        2. **.**git  디렉토리에 버전관리에 필요한 모든것이 들어있음.(숨긴파일) 
            - 그냥 ls로 하면 안보이지만 ls -a를 쓰면 숨긴파일까지 보임
2. touch README.md 로 파일을 만들어 줄 수 있음.
3. 특정 버전으로 남긴다 = “커밋(Commit)한다” - **3가지 영역을 바탕**으로 동작

# Staging Area

Commit을 할 때, 총 3가지 영역을 바탕으로 작동합니다.

- Working Directory : 내가 작업하고 있는 프로젝트의 디렉토리
- Staging Area : 커밋을 하기 위해 $ git add 명령어로 추가한 파일들이 모여있는 공간
- Repository : 커밋들이 모여있는 저장소

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/86f2e7ba-b6fe-47cb-81f8-4651ee44acf0/Untitled.png)

열심히 코드를 작성하다가 커밋을 해야하는 순간이 오면 **git add .**를 통해 커밋할 파일들을 추가합니다.

이 파일은 바로 Repository에 올라가지 않고, **Staging Area**에 올라가게 됩니다.

**Staging Area**에 추가한 파일들을**git Commit을 한다면 최종적으로 저장소(Repository)로  저장**되게 됩니다.

- **git status : 현재 상태 확인**

예시

git add README.md → git commit -m "Add README.md"

# TIL 프로젝트 실습