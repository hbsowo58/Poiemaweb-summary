React.createClass-> Class -> Hooks

리액트란 무엇인가? 왜 쓰는가?

사용자 인터페이스를 만들기 위한 JavaScript 라이브러리

Jqurey로도 웹을 잘만들었었다 그러나, SPA로 만들때 UX/UI를 향상시키고 (페이지 깜빡거림없애기)

앱같은 경험을 웹에서 구현, 데이터 처리를 쉽게하려고 데이터 <-> 화면 일치시키기

웹사이트 만들때, 중복되는 부분을 효율적으로 처리하기 위해서 (중복 처리, 유지보수) -> 컴포넌트화



1.사용자 경험 2.재사용 컴포넌트 3.데이터화면일치

---

리액트는 기본적으로 js파일 (html존재)  like-button.js



라이브러리 이기때문에 스크립트 필요



<script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script><script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>



리액트, 리액트돔 바로설치

class LikeButton extends React.Component

클래스로 만듬 -> construcor필요( 제일먼저 실행) -> 랜더부분이 화면그림



e('button', null, 'like'); <button>Like</button>



ReactDom 실제로 렌더링(반영)

ReactDom.render(e(LikeButton), document.querySelector('#root')) root 아이디에다 그리겠다



react는 루트가 필요하고, (컴포넌트들을 랜더링할) 상태(state)는 바뀌는, 바뀔 수 있는 부분이다.



this.state에 상태를 넣고, 그려줄때 this.setState로 찍는다 (상태변경 -> 화면변경)

(this.state를 construtor에 담는다)

class 하나가 컴포넌트 하나



babel(최신문법)

<script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>

<script type="text/babel">

스크립트 안에서 html이 가능하게됨 -> jsx (자바스크립트 +XML) -닫는괄호 필수



LikeButton (대문자 시작 => 컴포넌트) div -> html이다



<LikeButton /> 이것자체가 jsx인데 babel이 create.element로 만들어준다

리액트 ES6문법 지원 (클래스, 화살표함수)



최신 객체, 메소드 = 바벨 폴리필 사용







<h1>질문</h1>

리액트란 무엇인가? 왜 쓰는가?

사용자 인터페이스를 만들기 위한 JavaScript 라이브러리 , 1.사용자 경험 2.재사용 컴포넌트 3.데이터화면일치



babel의 용도는?

최신문법을 사용하기 위함 (아랫버전으로 자동변경)



jsx란?

자바스크립트 + xml (html태그를 스크립트 태그내에서도 사용할 수 있게해줌)



리액트는 최신문법을 지원하는가?

O



컴포넌트와 HTML태그를 구분하시오

1. LikeButton
2. div
3. Love
4. span

컴포넌트 , html태그, 컴포넌트 , 태그



리액트의 렌더링 방식 ?

1. 초기 렌더링 
   1. render 함수 
      1. 뷰 관련 정보가 담긴 객체를 반환
      2. 내부에 있는 컴포넌트들도 재귀적으로 렌더링
      3. 렌더링 작업 -> HTML 마크업 -> DOM 요소 안에 주입
2. 컴포넌트의 데이터 변경으로 다시 실행되는 리렌더링 
   1. 뷰를 업데이트 한다 -> '조화 과정을 거친다'
   2. 조화과정도 render 함수가 맡아서 한다. 
      1. 변경된 새로운 데이터를 가지고 render 함수를 또 다시 호출
      2. 이 때 render 함수가 반환하는 결과를 곧바로 DOM에 반영하지 않고 이전에 render 함수가 만들었던 컴포넌트 정보와 현재 render 함수가 만든 컴포넌트 정보를 비교
      3. DOM의 트리를 업데이트

리액트는 Angular와 같은 프레임워크와 혼용할 수 있을까?

A. 혼용가능. 라이브러리이기 때문에

JSX란?

A. 자바스크립트의 확장 문법이며 XML과 매우 유사

JSX의 장점 ?

A. 1 .보기 쉽고 익숙하다. 2. 활용도가 높다.(생성한 컴포넌트를 마치 HTML 태그를 사용하듯이 쓸 수 있다.)

리액트 컴포넌트에서 요소 여러 개를 하나의 요소를 감싸 주어야 하는 이유?

A. Virtual DOM에서 컴포넌트 변화를 감지해 낼 때 효율적으로 비교할 수 있도록 컴포넌트 내부는 하나의 DOM 트리 구조로 이루어져야 한다는 규칙이 있기 때문.

JSX 안에서 if문을 사용할 수 있을까?

A. 사용불가. 대신 삼항연산자를 사용하거나 JSX 밖에서 사용 가능.

JSX를 괄호로 감싸는 것은 필수사항일까?

A. 필수사항이 아니다. JSX를 여러 줄로 작성할 때 괄호로 감싸는 것이 일반적이다