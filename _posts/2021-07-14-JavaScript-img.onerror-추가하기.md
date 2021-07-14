---
layout: single
title: JavaScript로 HTML img.onerror 추가하기
categories: JavaScript
tag: [JavaScript,troubleshooting,html]
---

# 🎯 `<img>` 태그의 onerror 속성의 쓰임  

~~~html
<img src="메인 이미지 경로" onerror="this.src='대체 이미지 경로'">
~~~
>src에 등록된 이미지를 불러오는 데에 실패하면(400/404 Error 반환) 자동적으로 onerror에 등록된 스크립트가 실행됩니다. 위와 같이 src를 대체경로로 덮어씌우는 동작이 가능합니다. 
  
<br>

# 🧑🏻‍💻 JavsScript에서 onerror 등록

HTML에선 src와 onerror 모두 따옴표로 감싼 string의 형태라 Js에서도 비슷한 방식으로 등록하면 될 것 같지만, ***onerror***은 에러 발생시 실행되는 **script**이기 때문에 함수를 전달해줘야 됩니다. 

~~~js
const img=document.createElement("img");
img.src="main Path";
img.onerror="this.src='alternative Path'"   <== ❌

//Chrome 기준
img.error=(event)=>{
    event.target.src="alternative Path";    <== ⭕️
}
~~~
<br>

script이기 때문에 어떠한 동작도 가능합니다.  
이미지 로딩 실패시 alert만 띄어주는 것도 물론 가능합니다.  

~~~js
img.onerror=()=>{
    alert("Error Occurred");   
}
~~~

<br>

# ✔️ 확인   

Js로 `<img>` 태그의 onerror 속성을 추가했더라도 로딩된 화면의 html 소스에선 확인 할 수 없습니다.  
html을 동적 생성하는 과정에서 에러가 발생한다면 onerror 스크립트를 수행할 뿐입니다.  
만약 src를 덮어씌우는 스크립트였다면 동적 생성된 html에선 `<img src="대체경로">`만 있을 것입니다.