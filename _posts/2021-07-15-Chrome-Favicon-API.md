---
layout: single
title: Chrome Extension에서 Chrome Favicon API 사용하기
categories: JavaScript
tag: [JavaScript,html,Chrome Extension,troubleshooting]
---

> 결론부터 이야기하면 manifest.json에 permission을 추가해야됩니다.  
> Permission 설정 없이 `chrome://favicon/...`을 사용하면 로컬 경로 호출로 인식하여 **CORS 정책 위반 에러**를 만나게 됩니다.

<br>


# 🧑🏻‍💻 적용

아래와 같이 ***manifest.json***에 favicon permission을 등록하면 됩니다.

~~~json
{
  "permissions":[ "chrome://favicon/"],
  "content_security_policy": "img-src chrome://favicon;", 
  //<== Img의 source를 chrome://favicon...으로 제한하는 policy, 필수는 아니다.
}
~~~
<br>

권한 설정 이후론 아래와 같이 사용할 수 있습니다. 
~~~js
img.src=`chrome://favicon/size/24/${domain}`;
//favicon/size/크기(픽셀)/domain(url)
~~~

<br>

# ➕ 번외

같은 기능을 하는 구글 API 서버는 아래와 같습니다.  
Chrome API를 사용할 환경이 안된다면 아래 API URL을 사용하세요.

`https://www.google.com/s2/favicons?sz=24&domain=(도메인)`



