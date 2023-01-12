# *마크다운(markdown) 
텍스트 기반의 가벼운 마크업(markup) 언어.

텍스트만 이용해 문서의 구조/내용을 같이 쉽고 빠르게 적고자 탄생.

`markdownguide.org/cheat-sheet/`

참고하면 됨.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/625d200a-49f5-4a89-80e6-157b297ac01f/Untitled.png)

- markup ; 태그를 이용해 문서의 구조를 나타내는것.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9458bf4c-f343-4ec9-92da-a46d6abf6cfd/Untitled.png)

한 줄을 띄워야 함.

- [readme.md](http://readme.md) 파일을 통해 오픈 소스 공식문서 작성.

- .# 제목 혹은 소제목; Heading, 헤딩
    - 샵의 개수에 따라 제목의 수준 구별(h1 - h6)
    - 적을 수록
    - 글자 크기 키우기 위해서는 사용하면 안됨.
- 리스트. (1. 2. 3. or  - / * )
    - 순서가 있는 리스트, 없는 리스트
- 코드 블럭(```code block```   .`inline code block`.  ; 백틱(`)사용 )
    - 예시 할경우 `inline code block`
    - 특정 언어를 명시하면 구문 강조(syntax highlighting) 지원.
    - MM 이나 slack, 노션 에서도 사용 가능.
- 링크 ( [string](url) )
    - 스트링에서 보여지는 부분, url은 연결할 곳)
    - [이거는 그거지..]([[SSAFY] Public Document (notion.site)](https://www.notion.so/9dc94ea8a050472ca00ffe8ea58586da))
- 이미지( ![string](url) )
    - 이미지 삽입, 너비와 높이는 조절할수없음. 조절하기위해서는 HTML 사용
- 텍스트 강조
    - . **볼드할 글씨 . **  **볼드**
    - .* 기울림*.    *기울림*
    - ~ 가로선 ~, ~~가로선~~

- 수평선 - - - (————————————————————)
    - hypen ( - ), underbar( _ ) 로도 사용 가능.
- 표도 만들수 있음

|Syntax | Description |

| ----------- | ----------- |

| Header | Title |

| Paragraph | Text |

## **Git**

- `[README.md](http://README.md)`  프로젝트 설명문서!
- **Repository** ; 특정 디렉토리를 버전관리하는 저장소.
    - `git init`(initialize) 명령어로 로컬 저장소를 생성
    - .git 디렉토리에 버전관리에 필요한 모든 것이 있음.
        - .git < 앞의 . 때문에 숨김파일되어 있음.
    
    Working directory → Staging Area (commit 으로 남기고 싶은 내용)
    

                           **(`git add 파일명..`)**

Staging Area → Repository

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/84495ab3-c011-4f5f-891e-f339cc0a0c19/Untitled.png)

                           **(git commit) ; `git commit -m “ 남길 말 “` ;** 

                            **버전정보에 관한 정보**

git commit 할경우 staging area가 비게됨! 

- **`git status`** ; 현재상태 확인
- `git config --global [user.ema](http://user.email)il “ “`
- `git config --global [user.name](http://user.name) “ “`

`git remote add origin https://github.com/hyodeul/git_test.git`

`git remote -v`로 remote 연결되었는지 확인 가능.

Main or Master < 동일한 것이니 자료 찾거나 할때는 알아두기.

`git branch -M main`으로 이름 바꿀수 있음.

`git push -u origin main` 로 기존 local repository를 푸시.

현재 working directory와 commit된 버전 간 차이 확인하는 command ; `git diff 파일명`

(변경 후 commit하면 diff가 출력되지 않음!)

Repository → Remote Repository

                 **(git push) ; `git push origin main` 으로 푸시**

                 origin으로 main을 올리겠다.

`git log` ; git version 수정로그를 볼 수 있음.

→ commit 마다 고유 ID가 부여됨.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42507d69-2265-4214-8496-65d69372dce1/Untitled.png)

(Terminal ; local)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/df5dff55-97fb-4de5-bbcc-0b7cc7bb54fd/Untitled.png)

(Github; remote) , commit ID가 6자리만 기록됨.

= If ) bash command에서 벗어나고 싶다면 ? q 를 입력 =

`git commit` : 입력하면 **Vim** 으로 입력됨. 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/256a0ee8-049a-49ec-81fa-5523ee914ee5/Untitled.png)

당황하지 말고 

- `Esc` (명령모드)→ `:wq` 저장후 닫기 or `:q!` (저장하지 않고 강제종료)로 bash command 로 돌아갈수 있다!

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/70ec8d2d-4ce9-4cb7-93d1-2a6bea8a3c32/Untitled.png)

- `**git clone**` : github 등 저장되어있는 repo를 복제해옴.
    - `git clone "repo주소(https://github.com/hyodeul/git_test.git")` ;하면 현재디렉토리에 repo 에 저장된 폴더를 복사해옴 + `git init` & `git remote`같이 실행됨
- git clone 과 github 파일 다운로드 차이 : 변경내역이(.git 폴더) 포함되어있는지 여부.