# Tailwind CSS  set

### tailwind css 세팅 방법
세팅 방법으로는 총 4가지가 있다.

1. Tailwind CLI : Tailwind CLI 도구를 이용한 설치 방법으로 가장 빠르고 간결하다. 

    input.css 를 지정하면 그에 따른 output.css 가 나오게 되는 간단한 원리를 가지고 있다.
2. Using PostCSS : Webpack, Rollup, Vite, Parcel 과 같은 빌드 도구와 가장 깔끔하게 통합되는 방법이다.
3. Framework Guides: 프레임워크 가이드를 보고 세팅하는 것이다. 공식문서에 자세하게 나와있다.
4. Play CDN : CDN 을 이용하는 방법인데, 브라우저에서 간단하게 스크립트를 하나 추가하면 할 수 있다. 그러나 프로덕션에 권장되진 않고 개발용으로 사용하면 괜찮다

==> 1번 Tailwind CLI 도구 사용 환경 셋팅 (23.03.23.)


### Tailwind CSS CLI 셋팅 순서
1. node.js 설치하고 terminal에 ` npm init -y ` 입력
2. https://tailwindcss.com/docs/installation
링크에 나온 순서대로 진행

<details>
<summary>🧐 왜 Node.js를 설치해야하지?</summary>
<div markdown="1">

### 다음은 공식문서에서 소개한 node.js이다.

> Node.js는 Chrome V8 JavaScript 엔진으로 빌드된 JavaScript 런타임이다.

여기서 런타임이란 프로그래밍 언어가 구동되는 환경을 말한다. Javascript의 런타임은 Web Browser와 Node.js로 구성되어있다.

Node.js는 비동기 이벤트 기반(event-driven: 이벤트 호출에 따라 동작한다는 뜻), Non-Blocking I/O 모델을 사용해 가볍고 효율적이다. 때문에 비동기식 프로그래밍이 가능해서 I/O 부하가 심한 대규모 서비스를 개발하기 적합하다.

> 정리: Node.js는 백앤드 또는 웹 서버가 아니라 자바스크립트 실행 환경이다!

예전에는 자바스크립트 런타임이 브라우저 밖에 존재하지 않았는데, 그렇다면 Node.js는 어떠한 필요성에 의해 생기게 된 것일까?!

### 노드 탄생 배경
https://www.youtube.com/watch?v=EeYvFl7li9E
노드는 2009년 위 영상 속 Ryan Dhal이 고안해 낸 언어이다.

JSP나 PHP 언어로 웹 어플리케이션을 개발하면 이는 일반적으로 아파치와 같은 웹 서버에서 동작한다. 아파치는 쓰레드를 이용하여 다음과 같이 비동기를 처리한다.

어떤 클라이언트가 웹 서버에 연결을 요청
일정한 메모리 공간을 사용하여 새로운 쓰레드를 생성
아파치는 연결마다 쓰레드를 사용하므로 동시 연결이 많아질수록 메모리를 엄청 많이 사용할 수 밖에 없다. 따라서 더 많은 서버를 추가해야하고, 이는 단순 서버 비용 뿐만 아니라 운영 등에 발생하는 트래픽 비용, 인건비 등 여러 비용을 더하는 문제를 발생시킨다. 추가로, 여러 대의 서버를 사용하더라도 사용자 입장에서는 마치 하나의 서버에 접속하는 것과 같은 효과를 주어야 하기 때문에 모든 서버는 같은 데이터를 동기화해야 한다는 문제를 발생시키기도 한다.

바로 노드가, 이런 현실적인 문제를 해결하기 위해 등장했다.

### frontend에서 node.js?
npm으로 설치하는 모든 CLI(Babel, webpack, 걸프, CRA, Vue-CLI 등등)는 Node.js를 이용한다고 보면 된다.

[출처 바로가기](https://velog.io/@syoung125/%EA%B0%9C%EB%85%90%EA%B3%B5%EB%B6%80-2.-Node.js%EA%B0%80-%EB%AD%98%EA%B9%8C-package.json-npm-)
</div>
</details>