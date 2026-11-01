# OSS Assignment 4-1. REST API-Based CRUD Service with JavaScript

## 22200635 장영진

## Deployment: GitHub URL, Vercel URL, MockAPI Endpoint URL (비밀 키·비밀번호는 기록하지 않음)
GitHub URL: https://github.com/2026-2-OSS/assign09-c01-22200635
Vercel URL: https://assignment09-lilac.vercel.app
MockAPI EndPoint URL: https://6adea6dd4e88f1bba4a53a30.mockapi.io/Book

## Service: 주제, Field, CRUD 기능

도서 목록 관리 프로그램을 만들었다.
도서 정보를 등록, 조회, 수정, 삭제할 수 있다.
Field: 
1. bookId       6자리 도서 고유 번호 
2. title        도서명
3. genre        도서 장르
4. author       저자
5. publisher    출판사
6. status       대여 상태(대여 가능 / 대여 중)

CRUD기능:
1. Create   등록기능
- 새로운 도서 목록을 입력하고 서버에 등록한다.
- 도서 ID 중복 검사와 필수 입력값을 확인한다.
2. Read     목록조회
- MockAPI 서버에서 도서 목록을 불러온다.
- 등록된 도서 정보를 화면에 출력한다.
3. Update   수정
- 기존 도서 정보를 수정하고 서버에 반영한다.
4. Delete   삭제
- 선택한 도서를 서버에서 삭제한다.
5. Search   도서 제목 검색
- 원하는 도서의 제목을 입력하면 해당 도서만 출력
6. Error    에러
- 여러 오류 메시지를 try-catch를 활용함

## Key Learning: fetch(), JSON, async/await, REST API 등 배운 내용 3가지
1. fetch를 사용하여 MockAPI 서버와 데이터를 주고받는 법을 알게 되었다. 이를 실습을 통해 구현하여 동작 과정을 자세히 알게 되었다.
2. 실습 timer.html을 진행하며 타이머를 만들며 setInterval의 쓰임에 대해 알게 되었다.
3. async와 await를 사용하여 비동기 방식으로 처리하는 법을 알게 되었다.

## AI / Search Usage: 사용 내역과 본인 추정 AI 코드 기여율(%)
1. 기존 데이터를 불러와 수정하는 과정에서 patch를 사용하여 진행하고 있었는데 아무리 해도 모르겠어서 AI에게 무엇이 잘못되었냐고 물어보았다. 물어보니 특정 서버에서 PATCH 요청은 지원하지 않고 PUT 요청만 허용하는 경우가 있다고 했다. PATCH를 PUT으로 바꾸니 바로 해결되었다.

2. POST 구현 중 코드를 만들고 서버에 제대로 응답이 없는 것 같자 AI를 통해 함께 코드를 디버깅 하였고 이를 해결하였다. 

코드 기여율: 30%
## Problem & Solution / Reflection: 문제 해결 및 느낀 점
Problem: 도서 수정 기능을 구현하는 과정에서 PATCH 방식이 계속 오류가 발생함
Solution: PUT 메서드로 변경

Problem: 도서 삭제 후 목록이 정상적으로 갱신되지 않음
Solution: 오타 발견

Problem: 검색 기능을 구현하는 과정에서 검색 버튼을 구현하지 않음, form 밖에 있지만 검색 기능이 form안에 있다고 판단
Solution: 버튼을 구현하고, filter를 활용하여 구현

느낀점: 이번 과제를 통해 JavaScript에서 API 서버와 데이터를 주고받는 방법을 배울 수 있었다. 그전에는 항상 JS 내의 배열을 이용하여 데이터를 관리하여 목록이 커질수록 무거울 수 있지만 서버에서 따로 저장하니 이 문제가 해결된 것 같다.
두번째 수업을 참석하지 못해서 혼자 공부하여서 과제 구현에 애를 먹었지만 피피티의 예시와 실습 문제들을 따라가며 그대로 적용해보니 처음 생각했던 것 만큼 어렵지는 않았다. 