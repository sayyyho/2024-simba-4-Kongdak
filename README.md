# 콩닥콩닥

## 대학생활을 기억하는 방식을 바꾸다.

![readme_mockup2](./images/intro3.png)

<br>

## 프로젝트 소개

- 콩닥콩닥은 시간이 흐르면 그리워질 우리의 학창시절,입학부터 졸업까지 당신의 설렘을 간직해드립니다.
- 콩닥콩닥은 캠퍼스 건물 별로 나만의 일기를 기록할 수 있는 서비스입니다.
- 일기를 기록하고, 해시태그 기능과 랭킹 시스템을 통해 다른 사람들과 교류할 수 있습니다.
- 날씨 기능, 디데이, 업로드 수에 따라 달라지는 코끼리 이미지 등 소소한 디테일을 살려 서비스 이용에 재미를 더했습니다.

<br>

## 팀원 구성

<div align="center">

| ![zoey003](https://github.com/zoey003.png) | ![sayyyho](https://github.com/sayyyho.png) | ![chaem03](https://github.com/chaem03.png) | ![pyeree](https://github.com/pyeree.png) | ![onlynyang](https://github.com/onlynyang.png) |
| :----------------------------------------: | :----------------------------------------: | :----------------------------------------: | :--------------------------------------: | :--------------------------------------------: |
|    [김지현](https://github.com/zoey003)    |    [박세호](https://github.com/sayyyho)    |    [하채민](https://github.com/chaem03)    |   [임현우](https://github.com/pyeree)    |     [한지은](https://github.com/onlynyang)     |
|                기획/디자인                 |                 프론트엔드                 |                 프론트엔드                 |                  백엔드                  |                     백엔드                     |

</div>

<br>

## ✏️ 사용방법

## 🍎 Mac

### python 3.11 버전 설치

```SSH
https://www.python.org/ 에서 3.11 버전을 설치해주세요.
```

### python virtualenv를 이용한 가상환경 정의

```SSH
# 프로젝트를 생성하려는 폴더경로에서 git bash를 열고..
python3.11 -m venv venv
```

---

### 가상환경 실행 및 장고 설치

```SSH
source venv/bin/activate

# 최초 1회만
pip install django
```

---

### 프로젝트 실행

```SSH
# manage.py 포함된 경로에서
# Model을 건들이지 않았다면, 최초 1회만 실행
python manage.py makemigrations
python manage.py migrate

python manage.py runserver
```

---

## 💻 Windows

### python virtualenv를 이용한 가상환경 정의

```SSH
# 프로젝트를 생성하려는 폴더경로에서 git bash를 열고..
pip install virtualenv
virtualenv venv --python=3.11
```

---

### 가상환경 실행 및 장고설치

```SSH
source venv/Scripts/activate

# 최초 1회만
pip install django
```

---

### 프로젝트 실행

```SSH
# manage.py 포함된 경로에서
# Model을 건들이지 않았다면, 최초 1회만 실행
python manage.py makemigrations
python manage.py migrate

python manage.py runserver
```

## 1. 개발 환경

- PD : Figma ( [디자인 보러가기 ](https://www.figma.com/design/QoYerRSNVn6RwYx7aWuvUT/%EC%BD%A9%EB%8B%A5%EC%BD%A9%EB%8B%A5?node-id=2594-2732&t=dzkaXg1aOwc6rUh5-1))
- Frontend : HTML, CSS, JavaScript
- Backend : Python, Django
- 버전 및 이슈관리 : Github, Github Issues
- 협업 툴 : Discord, Notion

<br>

## 2. 협업 전략

### Git-flow 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다. - **main** 브랜치는 무결성 검증 이후 단계에서만 사용하는 브랜치입니다. - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다. - **Feat** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.

## GitHub Role

- 사용자는 먼저 Upstream Repository를 자신의 GitHub 계정으로 포크(fork)하고, 이 포크(fork)된 Origin Repository를 로컬 컴퓨터로 **Clone**하여 작업합니다.

- 그 후 개발한 변경 사항을 Origin Repository로 **Push**합니다. 이후 Upstream Repository로 풀 **PR**를 보내 변경 사항을 제안합니다.

- PR이 완료 된 후 Upstream Repository의 최신 변경 사항을 가져오기 위해 Local에서 풀(pull)을 사용합니다.

### 개발을 시작할 때

1. 개발을 시작할 때는 Upstream Repository에서 Issue를 생성합니다.
2. 이후 Issue에서 Origin Repository의 Dev Branch에서 새로운 Branch를 생성합니다
   - 이때 브랜치 이름은 다음을 따릅니다.
   - **새로운 기능 개발 : feature/#[Issue의 번호]**
   - **버그 픽스 : fix/#[Issue의 번호]**
   - **기능 리팩토링 : refactor/#[Issue의 번호]**
3. Loacl에서 Fetch를 통해 만든 New Branch(feature or fix or refactor)을 들고옵니다.
4. 해당 Branch로 checkout 이후 기능 개발을 진행합니다.

### 개발을 종료할 때

1. 기능 개발이 종료되면 Origin Repository의 Branch(feature or fix or refactor)로 변경 사항을 Push 합니다.
2. Origin Repository에서 Upstream Repository로 PR을 보냅니다.
3. Code Review 이후 마지막으로 Approve한 사람은 **Squash And Merge**를 합니다.
4. PR이 **Squash And Merge**되면 Local에서는 dev Branch로 checkout합니다.
5. Local에서 Upstream Repository의 dev Branch를 pull 받습니다.
6. 마지막으로 Origin Repository의 dev Branch를 Update하기 위해 Push를 해줍니다.

### Main Branch가 갱신될 때

1. 만약 Release Version을 낼 때는 Upstream의 dev Branch에서 main Branch로 PR을 날립니다.
2. 해당 Repository의 모든 사용자가 Code를 재확인한 후 Merge를 합니다.

## Commit & PR Convention

| Commit Type | Description                                                    |
| ----------- | -------------------------------------------------------------- |
| Feat        | 기능 개발                                                      |
| Fix         | 버그 수정                                                      |
| Docs        | 문서 수정                                                      |
| Style       | 코드 formatting, 세미콜론 누락 등 코드 자체의 변경이 없는 경우 |
| Refactor    | 코드 리팩토링                                                  |
| Chore       | package manager 수정 등                                        |
| Design      | CSS 등 사용자 UI 변경                                          |

  <br>

## 3. 프로젝트 구조

```
├── README.md
├── LICENSE
├── .gitignore
├── project
│   ├── .gitignore
│   ├── db.sqlite3
│   ├── manage.py
│   ├── Pipfile
│   ├── project
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   ├── static
│   │   │   ├── assets
│   │   │   │   ├── font
│   │   │   │   │   ├── Sagak-sagak.ttf
│   │   │   │   │   ├── Human-beomseok.ttf
│   │   │   │   ├── images
│   │   │   │   │   ├── a_screen.svg
│   │   │   │   │   ├── arrow.svg
│   │   │   │   │   ├── b_screen.svg
│   │   │   │   │   ├── ...
│   │   │   ├── css
│   │   │   │   ├── base
│   │   │   │   │   ├── index.css
│   │   │   │   │   ├── reset.css
│   │   │   │   ├── shared
│   │   │   │   │   ├── topnav.css
│   │   │   │   ├── all_posts.css
│   │   │   │   ├── category_a.css
│   │   │   │   ├── category_b.css
│   │   │   │   ├── category_c.css
│   │   │   │   ├── categorypage.css
│   │   │   │   ├── create_post.css
│   │   │   │   ├── edit.css
│   │   │   │   ├── login.css
│   │   │   │   ├── main.css
│   │   │   │   ├── post_detail.css
│   │   │   │   ├── search.css
│   │   │   │   ├── signup_done.css
│   │   │   │   ├── signup.css
│   │   │   ├── js
│   │   │   │   ├── allPost.js
│   │   │   │   ├── backControl.js
│   │   │   │   ├── category.js
│   │   │   │   ├── createPost.js
│   │   │   │   ├── editPost.js
│   │   │   │   ├── login.js
│   │   │   │   ├── main.js
│   │   │   │   ├── placeFrame.js
│   │   │   │   ├── postDetail.js
│   │   │   │   ├── search.js
│   │   │   │   ├── signup.js
│   │   │   │   ├── topnav.js
│   │   │   │   ├── weather.js
│   │   ├── templates
│   │   │   ├── shared
│   │   │   │   ├── _topnav.html
│   │   │   ├── base.html
│   └── main
│       ├── __init__.py
│       ├── admin.py
│       ├── apps.py
│       ├── forms.py
│       ├── models.py
│       ├── tests.py
│       ├── urls.py
│       ├── utils.py
│       ├── views.py
│       ├── templates
│       │   ├── all_posts.html
│       │   ├── cateogrypage.html
│       │   ├── create_post.html
│       │   ├── edit_post.html
│       │   ├── firstpage.html
│       │   ├── mainpage.html
│       │   ├── post_detail.html
│       │   ├── search.html
│       │   ├── secondpage_a.html
│       │   ├── secondpage_b.html
│       │   ├── secondpage_c.html
│       │   ├── signup_done.html
│       │   ├── signup.html

```

<br>

## 4. 주목할 부분
-  협업 방식 
-  최고의 순간 하트 구현
-  페이지 간 경로 


## 5. 페이지별 기능
### [초기화면]
![image](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/8d2d6337-cc31-4e9d-ab90-a38b873fc771)
   - 회원가입과 로그인을 할 수 있는 초기 화면 입니다.
   - 디자인
      - 로고 :심작 박동 수와 동국대학교의 명진관&남산타워를 조합해 콩닥콩닥만의 로고를 표현하였습니다.
      - 스타일 : 일기 작성을 컨셉으로 스케치북의 로그인 화면을 표현하였습니다.

### [회원가입]
![회원가입영상 - Clipchamp로 제작](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/bec7735e-2929-483c-a040-fcf275ab9256)

   - 아이디를 입력한 후 중복확인 버튼을 누르면 유효성 검사가 진행되고 통과하지 못한 경우 경고 문구가 입력창 하단에 표시됩니다. 
   - 비밀번호는 영문 / 숫자 포함 8글자 이상 입력해야하며, 비밀번호 확인란으로 유효성 검사를 합니다. 비밀번호가 일치하지 않거나, 영문 / 숫자 포함 8글자 이상이 아닐 시 각 입력창이 빨간색으로 표현되고 하단에 경고 문구가 표현됩니다.
   - 이름을 입력 받습니다.
   - 학번은 10자리로 입력해야하며 조건을 충족하지 않을 시 입력창 하단에 경고 문구가 표현됩니다.

### [로그인]
![로그인화면 - Clipchamp로 제작](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/b4711599-15bf-4066-bfa3-d3f258b01e5c)
   -  아이디와 비밀번호를 입력 받습니다. 로그인 버튼을 통해 유효성 검사를 실시하며, 유효하지 않은 아이디/비밀번호일 경우 입력창이 빨간색으로 표현되고 하단에 경고 문구가 표현됩니다.

### [로그아웃]
![제목 없는 동영상 - Clipchamp로 제작](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/14179ae5-55fa-429b-b309-0946412873fa)
   - 메인페이지 최 하단에 로그아웃 버튼을 통해 로그아웃 할 수 있습니다.
   - 로그아웃 버튼을 누르면 확인 메세지를 통해 사용자의 로그아웃 의사를 재 확인합니다.

### [메인페이지]
0. 상단 nav-bar
   
![image](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/92caa48b-9533-4c6e-8e60-f03dffc503e0)

   - "00일째 콩닥콩닥 "가입한 날짜로부터 경과한 날이 표현됩니다.
   -  현재 날짜와 오늘의 날씨가 실시간으로 연동됩니다.
     
1. 학교 맵
   ![image](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/118ba8f6-cf4a-4fa5-b8c4-c7c4b88102f2)

   - 실제 학교를 구조를 표현했으며 ,a, b, c 구역으로 나눠져  있으며 맵 하단에 건물들이 분류 되어 있습니다.
   - a, b, c 버튼을 통해 해당 구역 맵으로 이동할 수 있습니다. 사용자는 해당 구역의 건물을 선택해 건물별로 글을 남길 수 있습니다.
     
2. 해시태그 검색
   - 해시태그 검색 페이지로 이동할 수 있습니다.
     
3. 주간랭킹
   - 월요일 부터 일요일까지 1주일을 기준으로 주간 랭킹이 표현됩니다. 랭킹을 통해 사용자의 참여를 유도할 수 있습니다.
     
4. 내 정보
   
![image](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/e5717e58-9a7a-4a94-b9a3-0f28447cf576)

   - 회원가입 시 입력 했던 정보를 바탕으로 학번, 이름이 표현되고, 회원 가입일을 입학 날로 표현 됩니다. 추가로 사용자가 작성한 글의 개수를 표현합니다.
   - 사용자가 작성한 글 개수를 기준으로 개수별 코끼리 이미지가 변합니다.

5. 최고의 순간들
   - 모아보기 페이지에서 하트 버튼을 통해 사용자가 최고의 순간으로 지정한 글들을 개수 제한 없이 표현해줍니다
   - 글을 작성한 날짜와 제목, 건물이 표현 되며, 건물별 프레임은 a,b,c 구간 별로 다른 색으로 표현됩니다.
     
6. 모아보기
   - 사용자가 작성한 모든글을 한눈에 볼 수 있는 모아보기 페이지로 이동합니다.

### [Top-nav]
   - 뒤로가기 버튼을 통해 이전 페이지로 이동합니다.
   - 홈 버튼을 통해 메인페이지로 이동합니다.

### [구역 a,b,c 맵]
   - 메인페이지의 a,b,c 버튼을 통해 해당 구역 맵으로 이동합니다.
   - 사용자는 글을 남기고 싶은 건물을 선택해 해당 건물 페이지로 이동할 수 있습니다.

### [건물별 일기장]
1. 누적글 코끼리 순위

![image](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/02054676-60a8-4b37-adf8-4506f9efac4a)

   - 해당 건물에서 글을 많이 작성한 사용자 순으로 1위~3위까지 사용자 아이디와 게이징 바,작성한 글 개수로 표현됩니다.
     
2. 나의 글 목록
   - 실선 기준 상단에 사용자가 작성한 글 개수가 표현됩니다
   - 실선 기준 하단에 사용자가 작성한 글의 목록이 표현됩니다. 글은 작성한 날짜와 글의 제목 그날의 날씨가 표현됩니다.
   - 글을 선택하면 글을 수정 삭제할 수 있는 상세 페이지로 이동합니다.
   - 페이지 하단의 새로운 '추억 남기기' 버튼을 통해 건물에서 새 글을 작성할 수 있습니다.

### [글 작성]

![글작 - Clipchamp로 제작](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/41667f09-0c6e-4e5a-8301-23af77192346)

   - 현재 날짜와 현재의 날씨가 반영되며 사용자는 제목과 내용 해시태그를 입력할 수 있습니다.
   - 제목과 내용은 필수 입력이며 태그는 필수 입력이 아닙니다.
   - 제목은 8글자로 제한되며, 내용은 제한이 없습니다. 태그는 #을 붙이지 않고 작성후 엔터를 누르면 자동으로 # 붙습니다.
   - 유효성 검사 후 글 작성이 유효할 시 저장 버튼이 회색에서 주황색으로 활성화 됩니다.
   - 해시태그를 통해 사용자간의 상호작용을 유도하였습니다.

### [해시태그 검색]

![태그검 - Clipchamp로 제작](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/c73739b8-3204-4def-b229-0511f39e94c9)


   - 상단의 검색란에 글작성 페이지와 마찬가지로 원하는 해시태그 검색어를 입력후 엔터를 누르면 #이 붙습니다.
   - 입력 후 돋보기 버튼을 통해 검색을 할 수 있습니다
   - 검색 결과로는 해당 해시태그가 포함된 전체 사용자의 글이 최신순으로 업로드 됩니다.
   - 해당 해시태그가 포함된 전체 사용자의 글 내용을 볼 수 있습니다.
   - 해시태그 검색 결과가 없을 경우 '검색결과가 없습니다'로 표현됩니다.


### [글 상세 페이지]
1. 수정
   - 연필 버튼을 통해 글을 수정할 수 있습니다. 
2. 삭제
   - 휴지통 버튼을 통해 글을 삭제할 수 있습니다.
   - 로그아웃 버튼과 마찬가지로 사용자의 삭제 의사를 메시지를 통해 재 확인합니다.
  
### [모아보기]
- 사용자가 작성한 모든 글을 한눈에 볼 수 있으며, 날짜별 필터링 그리고 최고의 순간을 지정할 수 있습니다.
1. 기간 별 필터링 기능
   ![필터](https://github.com/LikeLion-at-DGU/2024-simba-4-Kongdak/assets/163874934/1fdcd4b5-f3cf-447f-8894-e50ec5cb851b)

   - 0000년, 00월 , 00일 ~ 0000년, 00월 , 00일 로 글을 필터링 합니다.
   - 기간을 지정 후 돋보기 버튼을 통해 필터링을 할 수 있습니다.
   - Reset 버튼을 통해 필터링을 초기화 할 수 있습니다.
2. 최고의 순간들 지정
   - 하트 버튼을 통해 최고의 순간들을 지정합니다.
   - 최고의 순간의 글은 메인페이지 '최고의 순간들' 확인 할 수 있습니다.

## 4. 개발 기간 및 작업 관리

### 개발 기간

- 전체 개발 기간 : 2024-06-16 ~ 2024-06-26

<br>

### 작업 관리

- GitHub Issues를 사용하여 진행 상황을 공유했습니다.
- 매일 스크럼 회의를 진행하며 작업 순서와 방향성에 대한 고민을 나누고 노션에 회의 내용을 기록했습니다.

<br>

## 5. 팀원별 역할 분배

### 김지현

- **프로젝트 기획 및 디자인 제작**

### 박세호

- **기능구현**
    - 회원가입,메인,글작성,글모아보기페이지 html, css, js구현

### 임현우

- **기능구현**
    - 태그 검색, 태그 작성, 기본 CRUD 설계(글 작성, 수정, 삭제) 및 기능구현, 날씨 API 설정, 회원가입 페이지 설계, 글 본문 보기 페이지 기능, 메인페이지 프로필 기능

### 하채민

- **기능구현**
    - 로그인, category, 건물별, 디테일post,  검색페이지 html, css, js 구현

### 한지은

- **기능구현**
    - 전체 페이지 연결 url 설계, 글 북마크 기능, 글 모아보기 페이지 설계 및 기능구현, 검색 시 필터 기능, 북마크 목록 설계 및 기능구현, 회원가입 중복확인 기능
