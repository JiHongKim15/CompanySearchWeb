# TEAM
- SSAFY 3기 광주 2반 201조 싸피탈출넘버원
- **팀장** 노경준
- **팀원** 이로운이, 정현석, 노순건, 이완희 김지홍


# 실행 환경 & 방법
### 실행
Window 10 Chrome
1. STS - Spring boot 실행
2. https://localhost:8080 접속

--> 추후 AWS를 통해 클라이언트 배포
### 환경설정
1. STS

2. VS code
  -> Frontend 폴더 cmd 실행
  -> yarn install
  -> yarn serve(실행)
  -> npm install --save vue-session(세션사용)
  -> yarn add core-js(세션 사용)

  -> vue add vuetify(vuetify 설치)

  

3. vue-bootstrap

# 프로그램 기능
### 취준생을 위한 검색 & 블로그 웹 사이트
# 제품 기능 소개

### 기업 검색을 통해 정보를 공유하는 취업준비 블로그

#### 1.  Mainpage

- 기업 검색
  - Admin이 만들어 둔 기업 리스트 검색 가능
  - 존재하지 않을 시 메세지 전송

2. Header

- 로고
  - 클릭 시 메인 페이지로 이동
- 로그인
  - 이메일, 패스워드 유효성 검사
    - 유효성 일치 시 하단 바 변경 및 로그인 버튼 활성화
  - 비밀번호 찾기 기능
    - 이메일로 비밀번호 전송
- 회원가입
  - 이메일, 패스워드 유효성 검사
    - 유효성 일치 시 하단 바 변경
  - 이메일 인증
    - 30분 내에 인증하지 않을 시 재인증 필요
  - 이메일, 아이디, 패스워드, 약관 동의 후 회원가입 버튼 활성화

#### 3. MyPage

- 내가 쓴 글 목록
  - 기업 별 목록 분류
  - 해당 글로 이동 가능
- 내 정보 보기 / 회원 정보 수정
  - 이메일, 닉네임 수정 불가능
  - 비밀번호 수정 가능
  - 프로필 사진 업로드
    - 업로드 시 사진 미리보기
  - 자기소개 등록
- 기업 목록
  - 검색할 수 있는 기업 목록 확인 가능
- 포스팅하기
  - 기업명, 기업정보(카테고리) 제목, 내용 입력 후 수정
  - 기업 검색에서 글쓰기 이동 시 자동으로 기업명 입력
  - 마크다운 형식으로 작성

#### 4. Searchpage

- 검색 기업 표시
- 한줄요약
  - Admin만 수정 가능
  - 수정 버튼 클릭 시 해당 페이지에서 입력창이 나타나 수정 가능
- 기업 공식 정보
  - Admin만 수정 가능
  - 마크다운 형식으로 제공
  - 수정 버튼 클릭 시 해당 페이지에서 입력창이 나타나 수정 가능
- 오픈 데이터
  - 로그인을 한 사용자라면 누구나 수정 가능
  - 비회원인경우, 읽기만 가능
  - 마크다운 에디터와 뷰를 활용
  - 수정 버튼 클릭 시 해당 페이지에서 입력창이 나타나 수정 가능
  - 수정 중 다른 사용자가 데이터를 이미 수정했다면, 수정 불가능
- 취업과 관련된 게시판 형성 (Community)
  -  모든 게시판, 베스트 글, 최근 이슈, 스터디 모집 4가지의 게시판 구현
    - 카테고리에 따라 분류
  - 블로그 제목, 카테고리, 글쓴이, 작성일자, 조회수, 좋아요를 포함
  - 조회수, 좋아요를 기반으로 정렬 기능 구현
  - 페이지네이션 구현
  - 로그인 시 글쓰기 가능
    - 포스트 페이지로 넘어감 & 기업 명 자동 입력
  - 표의 row 클릭 시 해당 글의 detail로 이동

#### 5. Blog

- 글을 쓴 사용자의 프로필, ID 표시
- 마크다운 형식으로 내용 표시
- 조회수, 댓글, 좋아요 수 확인
- 좋아요 클릭 시 좋아요 증가
- 댓글 기능
  - 개인 프로필 이미지 구현
  - 댓글 기능 구현

#### 6. admin page

- 유저 목록 조회 기능
  - 해당 유저가 쓴 블로글 작성글 확인 가능
- 게시글 조회 기능
- 기업
  - 기업 추가
  - 기업 삭제
  - 기업 조회
- 카테고리 관리
  - 카테고리 추가
  - 카테고리 삭제

#### 7. error 페이지 구현

- 에러 표시
  - 에러 코드 표시
- 이전페이지/메인페이지로 이동 가능


# 개발 환경
1. Window 10
2. STS - Spring Boot
3. Vue, yarn, axios
4. Java, REST API, MyBatis
5. HTML, CSS, Bootstrakp
6. MariDB

+) Git, Jira 협업 툴 이용


# 코드
MVC 패턴
### BackEnd(BE)
#### 1. DTO/VO
- User
    - Users: 로그인
    - SignupRequest: 회원가입
- Blog
    - Blog: 게시글 번호, 키워드, 블로그 제목, 내용, 글쓴이, 좋아요, 조회수, 작성시간
    - BlogResponse: Blog list와 Keyword 구분하여 전달
#### 2. Service
#### 3. Dao
- UserSignup: 회원관리 CRUD MyBatis 연동
- BlogDao: Blog CRUD MyBatis 연동
#### 4. Controller
- AccountController: 회원 관리
- BlogController: 블로그 관리
#### 5. mappers
- blog.xml: Blog CRUD MyBatis
- user.xml: 회원 CRUD MyBatis

### FrontEnd(FE)
#### page
##### blog
- MyList: 로그인 한 회원의 글 쓴 리스트 출력
##### user
- Join: 회원가입
- Login: 로그인
- Update: 회원수정
#### components\common
- Header: 네이게이션바 & 로그인, 로그아웃
