# vue를 이용한 포트폴리오 사이트 만들기
[사이트 바로가기](https://vue-project1109.vercel.app/)

## 기본 셋팅

🥨 터미널에서 최신버전 vue 다운로드
`npm init vue@latest`

🥨 셋팅
√ Project name: ... vue-project  
√ Add TypeScript? ... `No` / Yes  
√ Add JSX Support? ... No /`Yes`
√ Add Vue Router for Single Page Application development? ...  
No / `Yes`  
√ Add Pinia for state management? ... `No` / Yes  
√ Add Vitest for Unit Testing? ... `No` / Yes  
√ Add an End-to-End Testing Solution? » `No`  
√ Add ESLint for code quality? ... clsNo / `Yes`
√ Add Prettier for code formatting? ... No / `Yes`

🥨 폴더 이동
`cd vue-project`

🥨 다운로드
`npm install`

🥨 포맷
`npm run format`

🥨 실행
`npm run dev`

🥨 빌드
`npm run build`

## 추가 설치

### 1. GSAP

gsap 설치 : `npm install gsap`

GSAP (GreenSock Animation Platform)은 JavaScript로 웹 애니메이션을 개발하기 위한 강력한 라이브러리로, 웹 요소의 위치, 크기, 스타일 및 다른 속성을 부드럽게 조절하고, 시간에 따라 다양한 애니메이션 효과를 쉽게 구현할 수 있습니다. GSAP는 애니메이션의 시작, 일시 정지, 재생, 역방향 재생과 같은 시간 제어를 제공하며, 이질적인 타이밍과 속도 조절이 가능합니다. 또한 다양한 속성 유형을 다루며 플러그인을 지원하여 더 다양한 애니메이션 효과를 추가할 수 있습니다. GSAP는 웹 개발자들 사이에서 인기가 높으며 웹 애니메이션을 효과적으로 구현하고 관리하는데 도움을 줍니다.

### 2. sass

sass 설치 : `npm install sass`

Sass는 Syntactically Awesome Stylesheets의 약자로, CSS의 확장 언어로 사용됩니다. 이 스타일 시트 언어는 CSS보다 강력하며 유지 보수가 쉽도록 도와줍니다. Sass는 변수, 중첩 규칙, 믹스인 및 함수와 같은 고급 스타일링 기능을 제공하여 코드 재사용성을 높이고 가독성을 향상시킵니다. 또한, Sass 파일은 .sass 또는 .scss 확장자로 저장되며, 컴파일러를 사용하여 일반 CSS로 변환할 수 있습니다. 이러한 기능은 웹 개발자에게 더 효율적이고 유연한 스타일링 옵션을 제공합니다.

### 3. lenis

lenis 설치 `npm i @studio-freight/lenis`

lenis.js란 javascript로 작성 된 오픈소스 웹 프레임 워크입니다.
웹페이지에서 부드러운 스크롤을 가능하게하는 라이브러리입니다. 경량(~3KB), 빠른 스크롤을 지원하며 다른 애니메이션 라이브러리들과도 잘 연동되는 장점이 있어 많은 주목을 받고있는 라이브러리입니다.

## 배포
https://vercel.com/zeroins-projects
