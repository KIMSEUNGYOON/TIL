# a링크와 Link to 페이지 이동의 차이

## a태그

1. 페이지 이동을 하면서 새로운 데이터를 다시 불러오게 되며 href를 사용해 경로를 지정해줄 수 있다.
2. 상태 값을 잃고 속도가 저하된다.
3. 리액트 앱의 상태들도 초기화되고, 렌더링된 컴포넌트도 모두 사라지고 새로 렌더링을 하게 된다.

## Link 태그

1. Link태그는 HTML5 History API를 사용해서 브라우저의 주소만 바꿀 뿐, 페이지를 새로 불러오지는 않는다.
2. 데이터를 필요한 부분만 불러들일 수 있어 속도향상에 도움이 된다.
3. 재렌더링 되지 않고 바뀌어야 하는 화면만 재렌더링 되고 나머지 데이터는 그대로 유지된 채 재사용된다.
