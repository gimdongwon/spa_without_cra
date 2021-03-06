# 검색서비스

총 4가지 홈, 알람, 메모, 사진 기능 구현완료 하였습니다.

webpack을 통해 spa 구조를 설정하였고 route에 맞는 hbs 페이지를 불러와 해당 페이지에 맞는 script를 동적으로 로드하는 방식으로 개발하였습니다.

실행 방법은 해당

1. github repository를 clone한 후
2. 저장한 폴더로 이동 후 npm install로 필요한 모듈을 다운로드 한 후
3. npm start를 webpack서버를 실행 후 local server에 접속하신 후
4. 개발한 기능들을 확인하면 됩니다.

## 파일 구조

![alarm](https://raw.githubusercontent.com/gimdongwon/11st_homework/main/images/file.png)

webpack.config.js와 router.js 에서 spa관련된 설정을 한 후

index.js에서 추가 설정과 최상단 index.js와 하단 css, js를 load를 하는 방식으로 개발하였습니다.

index.html이 최상단 웹페이지 역할을 하고 handlebars를 통해 하위 페이지를 로드하였습니다.

## 아쉬운 점

1. 앱이다 보니 css를 처음에 휴대폰 사이즈로 고정해서 개발하다보니 오히려 반응형에 익숙한 저에게 좀 더 난관이었습니다.
2. 앱 이동을 통한 자유로움은 존재하나 script로 dom을 구성하니 리로드 했을 때 페이지가 갱신되지 않습니다. 하지만 localStorage에 저장하여 홈에서 다시 앱에 방문시 무리 저장된 상태로 이용할 수 있습니다.
3. 알람을 삭제한 후 해당 알람을 clearTimeout을 걸어주어야 했으나 index를 캐치하지 못하여 node는 삭제 되지만 setTimeout이 걸리지 않아 알람은 동작합니다.
4. netlify 배포를 통해 굳이 clone하지 않고 웹사이트에서 확인할 수 있도록 배포를 시도해보았으나 dist 파일을 정확히 읽지 못하여서 제대로 동작하지 않습니다. 배포에 대한 공부 필요성을 느꼈습니다.
5. 간단한 백엔드 서버를 도입하는게 맞는건지 정확한 판단이 스지 않아 개발하지 않았는데 새로고침과 local img 문제를 겪고 간단한 서버가 필요했던 것으로 인지하였습니다.

## 주의사항

1. 페이지 이동 후 새로고침 하면 페이지를 받지 못합니다. 다시 홈으로 가서 새로고침을 하고 해당 페이지에 다시가면 localStorage에 해당 작업 내용들이 저장되어 있습니다.

## 캡쳐

### Home

![home](https://raw.githubusercontent.com/gimdongwon/11st_homework/main/images/home.png)

### Alarm

![alarm](https://raw.githubusercontent.com/gimdongwon/11st_homework/main/images/alarm.png)

### Memo

![Memo](https://raw.githubusercontent.com/gimdongwon/11st_homework/main/images/memo.png)

### Picture

![Picture](https://raw.githubusercontent.com/gimdongwon/11st_homework/main/images/picture.png)
