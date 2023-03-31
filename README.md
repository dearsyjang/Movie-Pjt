<div align=center>
<img width="400" alt="image" src="https://user-images.githubusercontent.com/97591083/219679829-4a5e94b6-2453-4622-a7d7-b8d7f2144756.png">
</div>

## 목차
- [기획배경](#기획배경)
- [프로젝트 소개](#프로젝트-소개)
- [프로젝트 기간](#프로젝트-기간)
- [설치](#설치)
- [기능 소개](#기능-소개)
- [기술 스택](#기술-스택)
- [폴더 구조](#폴더-구조)

## 기획배경

- 문화생활과 취미생활에 대한 관심이 커지고 있는 현대 사회에 영화를 좋아한는 사람들이 하나의 웹 사이트에서 많은 서비스를 즐길 수 있도록 서비스를 기획하게 되었습니다. 영화에 대한 정보도 얻고 별점과 리뷰를 남길 수 있는 편리함과 커뮤니티 서비스를 통해 영화를 좋아하는 사람들이 모여 이야기를 나누어 소통과 재미를 느낄 수 있습니다.

## 프로젝트 소개

- 인기 있는 영화, 평점이 높은 영화, 최신 영화 등 모든 영화 정보를 얻고 평점을 남기고 오늘 밤 볼 영화를 추천 받을 수 있는 영화 커뮤니티 서비스

## 프로젝트 기간

- SSAFY 관통 페어 프로젝트 2022.05.20 ~ 2022.05.26 (7일)

## 설치

서비스를 사용하기 위해서는 다음과 같은 방법으로 실행합니다.<br/>
레포지토리를  clone 받습니다.

**[ BACK-END ]**

1. server 폴더 필요한 프로그램을 설치합니다.
```
pip install -r requirements.txt
```

2. 설치 완료 후, 백엔드를 실행합니다.

```
python manage.py runserver
```

**[ FRONT-END ]**

1. client 폴더에서 pacakge.json에 정의된 패키지 및 모듈을 설치합니다.

```
npm install
```
2. 설치 완료 후, 프론트엔드를 실행합니다.
```
npm run serve
```

## 기능 소개

| 구분                             | 기능                           | 설명                                    |
| ---------------------------------------------------------------- | -------------------------------------------------------------- | --------------------------------------- |
| 회원                             | 회원가입<br/>로그인<br/>로그아웃 | - 이름, 비밀번호, 비밀번호 확인   |
| 관리자                             | 영화 등록, 수정, 삭제<br/>유저 관리 권한 | - Django에서 제공하는 admin 기능   |
| 영화 정보                             | 영화 리스트 | - TMDB API 활용<br/> - 인기있는 영화, 평점 높은 영화, 최신 개봉 영화 리스트 조회   |
| 영화 정보                             | 개별 영화 정보 | - TMDB API 활용<br/> - 영화 포스터, 개봉일, 장르, 제작사, 제작국가, 줄거리, TMDB 평균 평점, Movie Night 평균 평점, Movie Night 평가에 참여한 사람 수 등 조회   |
| 영화 평점                             | 영화 별점 등록 | - ⭐ 0.5 ~ 5점 (0.5점 단위)로 별점 등록   |
| 영화 추천                             | 영화 추천 알고리즘 | - 사용자는 원하는 기간을 설정하고 그 기간 동안 자신이 주었던 최고 평균평점 장르와 최다 평점개수 장르 조회<br/> - 유저의 평점을 종합해 최고 평균평점 장르와 최다 평점개수 장르별 영화 추천<br/> - 추천 받은 영화들은 개봉일 오름차순, 내내림차순 / 평균 평점 오름차순, 내림차순 조회     |
| 커뮤니티                             | 게시판 | - 게시글(제목, 내용)을 작성, 수정, 삭제     |
| 커뮤니티                             | 게시글 | - 게시글 좋아요❤️     |
| 커뮤니티                             | 댓글 | - 댓글을 작성, 수정, 삭제     |
| 마이페이지                             | 사용자 | - 다른 사용자를 팔로우, 언팔로우<br/>- 팔로워, 팔로잉 수 조회<br/>-작성한 게시글, 작성한 댓글, 좋아요한 게시글 조회     |

### 💙 회원: 회원가입, 로그인
<div>
<img width="400" height="250" alt="signup" src="https://user-images.githubusercontent.com/97591083/228922530-637863b8-76fc-41e8-909e-874c93e7f452.png">
<img width="400" height="250" alt="login" src="https://user-images.githubusercontent.com/97591083/228930902-e80b16f5-a606-42b8-a060-265b37f2943a.png">
</div>

### 💛 홈 (HOME): 영화 순위 조회, 영화 평점등록
<img width="800" src="https://user-images.githubusercontent.com/97591083/228929238-412e2829-2809-4124-ae9c-d0f068d27e7b.gif">

### 💙 영화 추천 (MOVIES)
<img width="800" alt="movies" src="https://user-images.githubusercontent.com/97591083/228933573-559e2227-4112-4300-839a-4e200960c2d2.png">
<img width="800" src="https://user-images.githubusercontent.com/97591083/228934732-d48e094f-f3f0-48d8-9f36-25936057044d.gif")

### 💛 커뮤니티 (COMMUNITY): 게시글, 댓글, 좋아요
<div>
<img width="400" height="250" alt="article" src="https://user-images.githubusercontent.com/97591083/228931949-a16913e0-3806-4c29-9d0d-cc7b2c276214.png">
<img width="400" height="250" alt="comment" src="https://user-images.githubusercontent.com/97591083/228932130-6fde41ca-706e-4980-be64-9da369acecc2.png">
<img width="800" src="https://user-images.githubusercontent.com/97591083/229162660-8dcfb6d1-09ad-4262-a507-dd13511947a4.gif">
</div>

### 💙 마이페이지 (MYPAGE): 팔로우, 마이페이지 조회
<img width="800" alt="mypage" src="https://user-images.githubusercontent.com/97591083/229107698-3fe14a33-3220-41e1-99da-9a17e28bc921.png">
<img width="800" src="https://user-images.githubusercontent.com/97591083/229109085-5faae9e2-b3de-4f86-ba37-b7850c8fa3f9.gif">


## 기술 스택

**[ FRONT-END ]**

- **Vue 2.5**
- **JavaScript**
- **Node LTS**
- **HTML, CSS**
- **BootStrap 5.2.0**

**[ BACK-END ]**

- **Python 3.8**
- **Django 3.2**
- **TMDB API**

## 폴더 구조

**[ FRONT-END ]**

```
📁 client
├── 📁public
├── 📁src
│ ├── 📁assets
│ ├── 📁components
│   ├── 📁accounts
│     └──📄AccountErrorList.vue
│   ├── 📁communities
│     ├──📄ArticleAndCommentErrorList.vue
│     ├──📄ArticleForm.vue
│     ├──📄CommentCreateForm.vue
│     └──📄CommentList.vue
│   └── 📁home
│     ├──📄HomveViewItem.vue
│     └──📄NavBar.vue
│ ├── 📁router
│   └──📄index.js
│ ├── 📁store
│   ├── 📁modules
│     ├──📄accounts.js
│     ├──📄communities.js
│     └──📄movies.js
│ ├── 📁urls
│   └──📄djangourl.js
│ ├── 📁views
│   ├── 📁accounts
│     ├──📄LoginView.vue
│     ├──📄ProfileView.vue
│     └──📄SignUpView.vue
│   ├── 📁communities
│     ├──📄ArticleCreateView.vue
│     ├──📄ArticleUpdateView.vue
│     ├──📄ArticleView.vue
│     └──📄CommunityView.vue
│   ├── 📁movies
│     ├──📄MoviesDetail.vue
│     └──📄MoviesView.vue
│   ├──📄HomveView.vue
│   └──📄NotFound404.vue
│ ├──📄App.vue
│ └──📄main.js
├──📄babel.config.js
├──📄jsconfig.json
├──📄package-lock.json
├──📄package.json
└──📄vue.config.js
```


**[ BACK-END ]**

```
📁 server
│ ├── 📁accounts
│   ├── 📁migrations
│     ├──📄0001_initial.py
│     ├──📄0002_remove_user_followings.py
│     ├──📄0003_user_followings.py
│     └──📄__init__.py
│   ├──📄__init__.py
│   ├──📄admin.py
│   ├──📄apps.py
│   ├──📄models.py
│   ├──📄serializers.py
│   ├──📄tests.py
│   ├──📄urls.py
│   └──📄views.py
│ ├── 📁community
│   ├── 📁migrations
│     ├──📄0001_initial.py
│     ├──📄0002_comment_like_users.py
│     └──📄__init__.py
│   ├── 📁serializers
│     ├──📄article.py
│     └──📄comment.py
│   ├──📄__init__.py
│   ├──📄admin.py
│   ├──📄apps.py
│   ├──📄models.py
│   ├──📄tests.py
│   ├──📄urls.py
│   └──📄views.py
│ ├── 📁movies
│   ├── 📁fixtures
│     └──📄movies.json
│   ├── 📁migrations
│     ├──📄0001_initial.py
│     ├──📄0002_remove_movie_like_users.py
│     ├──📄0003_movie_like_users.py
│     ├──📄0007_alter_movie_like_users.py
│     ├──📄0010_rename_movies_rating_score.py
│     ├──📄0013_alter_movie_like_users.py
│     └──📄0014_rating_genre_ids.py
│   ├──📄__init__.py
│   ├──📄admin.py
│   ├──📄apps.py
│   ├──📄models.py
│   ├──📄serializers.py
│   ├──📄tests.py
│   ├──📄urls.py
│   └──📄views.py
│ ├── 📁server
│   ├──📄__init__.py
│   ├──📄asgi.py
│   ├──📄settings.py
│   ├──📄urls.py
│   └──📄wsgi.py
│ ├── 📄manage.py
│ └── 📄requirements.txt
```
