Web Application 자체에서 날씨 API와 통신할 때 API Key가 노출되는 것을 피하고 싶었습니다.
Front-end에서
Client-side에서 API key를 숨긴채 3rd Party API와 통신하는 것이 불가능함에 따라




# Reference

[Client-Side에서 Youtube API Key 숨기기
](https://velog.io/@bigsaigon333/Client-Side%EC%97%90%EC%84%9C-Youtube-API-Key-%EC%88%A8%EA%B8%B0%EA%B8%B0)

()
Html, Js, Css를 활용해서 간단한 To-do list를 만드는 도중 weather API를 사용해서 현재 위치의 날씨를 알려주고 싶었습니다. 
[OpenWeather](https://openweathermap.org/)에서 API 사용 신청을 하고 
[서버리스 핸들러](https://velopert.com/3549)

[핸들러.js 설명](https://medium.com/@jwyeom63/%EB%B9%A0%EB%A5%B4%EA%B2%8C-%EB%B0%B0%EC%9B%8C%EB%B3%B4%EB%8A%94-node-js%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-%EC%84%9C%EB%B2%84%EB%A6%AC%EC%8A%A4-serverless-503ee61539d4)

>functions속성은 서비스 내의 모든 함수들을 나열하고 있다. 여기서는 hello가 현재 hander.js 파일에 있는 유일한 함수이다. handler속성은 여러분이 실행하고자 하는 함수의 코드가 어느 파일 혹은 모듈에 있는지를 가리킨다. handler.js라는 이름으로 기본 파일이 생성된다. 매우 편리한 기능이다.
handler.js 를 열어보면 handler 모듈과 hello라는 이름의 함수를 볼 수 있을것이다. 이 함수는 세개의 파라미터를 받는다. event 파라미터는 함수에 넘겨진 이벤트 데이터이다. context 파라미터는 함수의 컨텍스트, 러닝타임, 상태(state) 등의 중요한 정보를 담고 있다. 마지막으로 callback은 어떤 데이터를 반환할 것인지를 뜻한다. 이 예제에서는 response가 콜백 함수의 두번째 파라미터로 지정되어있다. 첫번째는 언제나 에러이며, 에러가 없으면 null이 넘어온다.
