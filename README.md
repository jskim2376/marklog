# 마크다운 지원 블로그 MARKLOG

<img src="https://github.com/padomay1352/marklog/assets/19688616/c4528b66-3f2c-4ae0-96ea-6e83a0be5d1a" width="1024">

## 프로젝트 소개

- Marklog는 블로그 서비스로 Markdown을 지원하는 블로그입니다.
- social login을 통해 회원가입을 하고 다양한 글을 등록할 수 있습니다.
- 원하는 태그, 제목, 본문을 검색해 여러 글들을 탐색 할 수 있습니다.
- 마음에 드는 게시글에 좋아요를 누르거나 댓글을 작성할 수 있습니다.

## 시작하기

1. Clone repo

```consol
git clone https://github.com/padomay1352/marklog.git
```

2. run app

```consol
docker compose up
```

## 기술 스택

### Language & Framework

| Java | SpringBoot | JPA | JavaScript | TypeScript |
| --- | --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/jmnote/z-icons/master/svg/java.svg" width="64"> | <img src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/b2184cf3-3588-4975-b96b-6bc0bcd37841" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/91be41e4-5e2d-402a-bd1f-822f7c1e8fb9"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/ff39d084-909e-450f-829a-d8009e62fc5c"> |

### DevOps

| aws | nginx | docker | jenkins | github |
| --- | --- | --- | --- | --- |
| <img src="https://github.com/padomay1352/marklog/assets/19688616/8bbdcfe9-f093-489d-954c-587740c5aaea" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/a96f5881-cdb4-4409-9b67-1f2c132ecd96" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/85db1d09-d22d-4ebd-bfde-0fcdb48d8231" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/6fb4ca5d-ae01-4422-8977-47f9b4035e29" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/75807a34-e3f2-40d0-b768-72dfaaba91f2" width="64"> |

### Tools

| Figma | Google Slide |
| --- | --- |
| <img src="https://github.com/padomay1352/marklog/assets/19688616/ff4c8d69-2d16-4da3-9041-a1987ba78fd9" width="64"> | <img src="https://github.com/padomay1352/marklog/assets/19688616/05a94f36-cc7a-4757-ad13-1cc218661b1e" height="64"> |

# 기획

## IA

[IA](https://www.figma.com/file/cWF2H8crAdWf1Yp5naJ4F0/marklog-task-flow-chart?type=whiteboard&node-id=0%3A1&t=YWJvTzoz8Wnc1QmA-1)

<img width="9056" alt="marklog IA" src="https://github.com/padomay1352/marklog/assets/19688616/63411bd2-a579-4ef1-beef-86b67ee7d370">

## Wireframe

[Figma](https://www.figma.com/file/1rA8RYUvnwoo0JodcDA0Y6/Marklog-Wire-Frame?type=design&node-id=0%3A1&mode=design&t=ubbp4B2sbCpUfSuX-1)

![header](https://github.com/padomay1352/marklog/assets/19688616/2a4ff18b-166a-43d5-8459-ad794fceb2b9) ![footer](https://github.com/padomay1352/marklog/assets/19688616/395dd9d4-0089-4b2c-9853-45446122812b) ![page](https://github.com/padomay1352/marklog/assets/19688616/4b142275-bfa2-4308-acea-80dac9bd7a64)

## API Document

[API List](https://unmarred-popcorn-664.notion.site/519115b73fa2462d9fb3ff08d5568617?v=41a4c4b0073646d6a9c4ffdb7ae7d6a90) |Name|Select| |---|---| |/post|GET| |/post|POST| |/post/{id}|GET| |/post/{id}|PUT| |/post/{id}|DELETE| |/post/{id}/like|POST| |/post/{id}/like|DELETE| |/post/{id}/comment|GET| |/post/{id}/comment|POST| |/post/{id}/comment/{commentId}|GET| |/post/{id}/comment/{commentId}|PUT| |/post/{id}/comment/{commentId}|DELETE| |/search|GET| |/search/user|GET| |/search/tag|GET| |/token/check|GET| |/token/refresh|GET| |/user/logout|GET| |/user/{id}|GET| |/user/{id}|PUT| |/user/{id}|DELETE| |/user/{id}/notice|GET| |/user/{id}/notice|DELETE|

# 기능

    - 유저
        - 로그인(Google SSO), 로그아웃
        - 회원가입, 탈퇴
        - 유저 정보 조회/수정
        - 댓글/답글 알림
    - 게시글
        - 게시글 조회/등록/수정/삭제
        - 게시글 내용/제목/태그 검색
        - 좋아요
        - 댓글
            - 댓글 등록/삭제
            - 답글 등록/삭제
    - 블로그
        - 작성글 조회
