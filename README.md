# 마크 다운 지원 블로그 Marklog

![](https://i.imgur.com/daj4dGK.jpeg)

## 개요

| 소개      | Marklog은 마크다운을 지원하는 간편한 블로그 플랫폼입니다. |
| --------- | --------------------------------------------------------- |
| 개발 기간 | 2023.03 - 2023.06                                         |
| 플랫폼    | Web                                                       |
| 개발 인원 | 1명(개인 프로젝트)                                        |
| GitHub    | https://github.com/jskim2376/marklog                      |

## 사용 기술

| TypeScript, lit-html, Bootstrap | Frontend page 개발을 위해 사용했습니다.      |
| ------------------------------- | -------------------------------------------- |
| Java 8, Spring Boot             | Backend API 개발을 위해 사용했습니다.        |
| MySQL, JPA, QueryDSL            | 데이터 저장 및 Java ORM을 위해 사용했습니다. |
| Jenkins, Git, GitHub            | CI/CD를 위해 사용했습니다.                   |
| AWS, Docker, Nginx              | 서버를 배포하기 위해 사용했습니다.           |

## 프로젝트 구조

![](https://i.imgur.com/MPTqh0R.jpeg)

## IA

![marklog IA](https://i.imgur.com/1y4fpRV.jpeg)

## 와이어 프레임

![marklog wire frame](https://i.imgur.com/BIrVkte.png)

## ERD

![marklog erd](https://i.imgur.com/dfvheQW.png)

## API

| Name                           | Method | 설명                                            |
| ------------------------------ | ------ | ----------------------------------------------- |
| /post                          | GET    | 최신 게시글 개요를 페이지 단위로 조회합니다.    |
| /post                          | POST   | 게시글을 생성합니다.                            |
| /post/{id}                     | GET    | 좋아요 포함해 게시글을 조회합니다.              |
| /post/{id}                     | PUT    | 관리자 또는 작성자가 게시글을 수정합니다.       |
| /post/{id}                     | DELETE | 관리자 또는 작성자가 게시글을 삭제합니다.       |
| /post/{id}/like                | POST   | 게시글에 좋아요 생성합니다.                     |
| /post/{id}/like                | DELETE | 게시글에 좋아요 삭제합니다.                     |
| /post/{id}/comment             | GET    | 게시글의 댓글에 생성합니다.                     |
| /post/{id}/comment             | POST   | 게시글에 댓글을 삭제합니다.                     |
| /post/{id}/comment/{commentId} | GET    | 게시글에 댓글에 답글을 생성합니다.              |
| /post/{id}/comment/{commentId} | DELETE | 게시글의 댓글에 답글을 삭제합니다.              |
| /search                        | GET    | 제목과 내용으로 게시글을 검색합니다.            |
| /search/user                   | GET    | 사용자의 게시글을 검색합니다.                   |
| /search/tag                    | GET    | 태그로 게시글을 검색합니다.                     |
| /token/check                   | GET    | JWT 인증이 올바른지 확인합니다.                 |
| /token/refresh                 | GET    | refresh token으로 새 access_token을 발급합니다. |
| /user/logout                   | GET    | JWT Cookie을 삭제해 로그아웃 합니다.            |
| /user/{id}                     | GET    | 유저를 조회합니다.                              |
| /user/{id}                     | PUT    | 유저 정보를 수정합니다.                         |
| /user/{id}                     | DELETE | 유저를 삭제합니다.                              |
| /user/{id}/notice              | GET    | 알림을 받아옵니다.                              |
| /user/{id}/notice              | DELETE | 알림을 삭제합니다.                              |

## 페이지 목록

### home / blog

- 최신 게시글 목록의 썸네일을 확인 할 수 있습니다.
- 사용자의 블로그를 확인 할 수 있습니다.

| home                                             | blog                                     |
| ------------------------------------------------ | ---------------------------------------- |
| ![marklog blog](https://i.imgur.com/jcTivKA.png) | ![](https://i.imgur.com/K6oeCBW.png)<br> |

### search / tag

- 제목, 내용, 태그를 기반으로 한 상세 검색 기능을 개발하여 사용자가 쉽게 원하는 콘텐츠를 찾을 수 있습니다.

| home                                            | tag                                  |
| ----------------------------------------------- | ------------------------------------ |
| ![marklog tag](https://i.imgur.com/1B0FJ76.png) | ![](https://i.imgur.com/hBAyZUi.png) |

### post & delete / write & edit

- 게시글을 조회 및 삭제를 할 수 있습니다.
- 게시글에 좋아요와 댓글과 답글을 작성할 수 있습니다.
- 게시글을 작성하고 수정 할 수 있습니다.

| post & delete                            | write & edit                                           |
| ---------------------------------------- | ------------------------------------------------------ |
| ![](https://i.imgur.com/byMUZ0q.png)<br> | ![](https://i.ibb.co/MZ8XXdq/localhost-8080-write.png) |

### login & setting

- google SSO로 로그인 및 회원가입을 할 수 있습니다.
- 사용자의 이미지, 이름, 소개, 블로그 이름, 회원탈퇴를 할 수 있습니다.

| login                                                  | setting                                                  |
| ------------------------------------------------------ | -------------------------------------------------------- |
| ![](https://i.ibb.co/4S2rbSg/localhost-8080-login.png) | ![](https://i.ibb.co/hDghwwr/localhost-8080-setting.png) |
