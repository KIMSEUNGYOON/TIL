# 서버사이드 렌더링 vs 클라이언트 사이드렌더링

클라이언트 사이드 렌더링은 페이지의 내용을 브라우저에서 그리고 서버 사이드 렌더링은 서버에서 페이지의 내용을 다 그려서 브라우저로 던져준다.
서버 사이드 렌더링의 경우 브라우저에 대한 서버 응답은 렌더링 준비가 된 HTML 페이지인 반면, 클라이언트 사이드 렌더링의 경우 브라우저는 자바스크립트에 대한 링크가 있는 빈 문서를 제공한다.

## 서버사이드 렌더링

서버사이드 렌더링(SSR)은 페이지를 이동할 때마다 새로운 페이지를 요청한다.
모든 템플릿은 서버 연산을 통해서 렌더링하고 완성된 페이지 형태로 응답한다. 1.

### 장점

1. 검색엔진 최적화 (SEO) 가능서버
   사이드 렌더링을 통해 얻을 수 있는 가장 큰 장점
   검색 엔진 최적화란 구글, 네이버와 같은 검색 사이트에서 검색했을 때 결과가 사용자에게 많이 노출될 수 있도록 최적화 하는 기법
   특히, sns에서 링크를 공유했을 때 해당 웹 사이트의 정보를 이미지와 설명으로 표시해주는 OG(Open Graph) Tag를 페이지 별로 적용하기 위해서는 서버 사이드 렌더링이 효율적이다.
2. 빠른 페이지 렌더링
   빈 HTML 페이지를 받아 브라우저에서 그리는 클라이언트 사이드 렌더링과 다르게 서버에서 미리 그려서 브라우저로 보내주기 때문에 페이지를 그리는 시간을 단축할 수 있다. 즉, 클라이언트 사이드 렌더링보다 페이지 구성 속도는 느리지만 전체적으로 사용자에게 보여주는 컨텐츠 구성이 완료되는 시점은 빨라진다.

### 단점

1. 프로젝트의 복잡도
2. 서버 렌더링에 따른 부하가 발생
3. 불필요한 인터넷 대역폭이 소모될 수 있음
4. 페이지 요청마다 페이지 새로고침이 발생한다.
   ex)next.js

## 클라이언트 사이드 렌더링

클라이언트에서 렌더링하는 방식

### 장점

첫 요청할 때 한 페이지만 불러오게 된다. 그 후, 사용자의 행동에 따른 필요한 부분만 다시 읽어들이기 때문에 서버 측에서 렌더링하여 전체 페이지를 다시 읽어들이는 것보다 빠른 인터렉션을 기대할 수 있다.
즉, 필요한 부분만 리로딩 없이 서버로부터 받아서 화면을 갱신하게 된다.

### 단점

1. 초기 구동 속도가 느리다
2. 검색엔진 최적화가 어렵다.
   ex)react
