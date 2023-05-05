# Axios란

Axios란 브라우저, Node.js를 위한 PromiseAPI를 활용하는 HTTP 비동기통신 라이브러리이다. 백엔드와 프론트엔드와의 통신을 쉽게 하기 위해 Ajax와 더불어 사용한다

## axios 특징

1. 운영 환경에 따라 브라우저의 XMLHttpRequest 객체 또는 Node.js의 http ali 사용
2. Promise(ES6) API 사용
3. 요청과 응답 데이터의 변형
4. HTTP 요청 취소
5. HTTP 요청과 응답을 JSON 형태로 자동 변경

## 메소드 종류

1. GET
   axios.get(url,[,config])

-   입력한 url에 존재하는 자원에 요청을 한다.
-   서버에서 어떤 데이터를 가져와서 보여주는 용도

2. POST
   axios.post("url주소",{data객체},[,config])

-   새로운 리소스를 생성(create)할 때 사용한다.
-   post 메소드의 두 번째 인자는 본문으로 보낼 데이터를 설정한 객체리터럴을 전달한다
-   로그인, 회원가입 같은 사용자가 생성한 파일을 서버에다가 업로드할때 사용, 주소창에 쿼리스트링이 남지 않아 GET보다 안전하다.

3. Delete
   axios.delete(URL,[,config]);

-   Delete메서드는 HTML Form 태그에서 기본적으로 지원하는 HTTP 메서드가 아니다
-   Delete메서드는 서버에 있는 데이터베이스의 내용을 삭제하는 것을 주 목적으로 하기에 두 번째 인자를 아예 전달하지 않는다.

4. PUT
   axios.put(url[, data[, config]])
   REST 기반 API 프로그램에서 데이터베이스에 저장되어 있는 내용을 갱신하는 목적으로 사용됩니다.
