hooks는

객체에 담는형식이 아닌, 하나씩 쪼개는형식

state = { asdasd, asdasdasd, asdsa,}



const [state, setState] = React.useState(초기값) <- 애는 컴포넌트안에 넣어줘야한다

setValue 사용



ref사용시 current로 접근



구조분해 , 비구조화 변수자리에 배열사용 const [state, setState]

state가 바뀌면 Hooks전체가 다시 실행되서, class에 비해 느릴 수 있다. (함수도 재생성)

<-> class에선 render만 재실행



리액트에선 class불가 className, for 대신 htmlFor



객체형으로 setState 쌓지 않는이유 :각각변화시킬 때 문제생김



setResult('정답');

​        setFirst(Math.ceil(Math.random() * 9));

​        setSecond(Math.ceil(Math.random() * 9));

​        setValue('');



setstate 모아서 처리 (비동기 리액트가 알아서함) 그래서 여러번 출력하지않음





webpack을 왜쓸까?

컴포넌트가 여러개라면? 유지보수가 불가능하다

여러개의 자바스크립트파일을 하나의 자바스크립트 파일로 만든다



노드 = 자바스크립트 실행기 그이상 이하도 아니다

서버를 알아야된다가 아니라 웹팩을 돌리기 위함을 알아야한다



npm init (패키지.json)설치 및

npm i -D webpack webpack-cli



노드의 모듈시스템을 이용해서 설치한것을 불러온다



create.react.app = 직접세팅하는것을 대신해줌





js vs jsx 개발자들에게 도움이됨



  entry:{

  }, //입력

  output:{

  }, //출력

제일중요(웹팩)



명령어 등록이 안되어있을떄 : 명령어 등록 or 스크립트에작성 npm run (dev)





현재 리액트는 hook을 사용한다.

이전에는 class로 만들어졌고, 현재도 많이 사용하기 때문에 class도 이해가 필요하다.

create.class → class → hook

------

Hook은 함수 컴포넌트에서 React state와 생명주기 기능(lifecycle features)을 “연동(hook into)“할 수 있게 해주는 함수

Hook을 이용하여 Class를 작성할 필요 없이 상태 값과 여러 React의 기능을 사용할 수 있다.

Hook은 계층 변화 없이 상태 관련 로직을 재사용할 수 있도록 도와준다.

Hook은 class 안에서는 동작하지 않는다.

Hook을 사용하면 코드가 짧아지고 간결 해진다.

- React에 Hook을 도입한 이유

  - 컴포넌트 사이에서 상태와 관련된 로직을 재사용하기 어렵다. (코드의 재사용성)
  - 복잡한 컴포넌트들은 이해하기 어렵다. (코드의 가독성)
  - `this` 의 작동 방식을 이해해야 한다. (높은 진입장벽)

- Hook의 사용규칙

  - 최상위(at the top level)에서만 Hook을 호출 (반복문, 조건문, 중첩된 함수 내에서 Hook을 실행하지 말아야 한다.)
  - React 함수 컴포넌트 내에서만 Hook을 호출 (일반 JavaScript 함수에서는 Hook을 호출해서는 안 된다. 하지만 custom Hook에서는 가능하다.)

- 리액트에서 사용 할수 없는 어트리뷰트

  class → className

  for → labelFor

------

- Q. 리액트에서 class와 for 대신하여 사용하는 것

  A. className, labelFor

- Q. Hook을 사용하면 얻는 장점

  A.

  - class의 작성 없이 상태 값과 리액트의 여러 기능을 사용할 수 있다.
  - 코드가 짧아지고 간결 해진다.
  - 계층 변화 없이 상태관련 로직을 재활용 할수 있게 해준다

- Q. Hook을 사용할때 주의 할점

  A.

  - class안에서는 동작하지 않는다
  - 최상위에서만 hook을 호출 해야한다.
  - React 함수 컴포넌트 내에서만 Hook을 호출해야 한다.

- Q. Webpack의 핵심 적인 기능

  A. JavaScript 코드를 모듈화 하여 관리하기 쉽게 만들어 준다. (모듈 번들러)

- Q. Babel은 Webpack에 포함되어 있는 기능이다. ( O / X )

  A.

  X, Babel은 트랜스 파일러로 Webpack에 포함 되어있는 기능이 아니다.



## **질문**

- React Hooks에서 상태관리를 하기 위해서 사용하는 메서드는 ?

  A. React.useState()

- React Hooks에서 ref를 사용하기 위한 메서드는 ?

  A. React.useRef()

- React에서 html 속성 중 사용할 수 없는 속성 두 가지와 대체하는 속성명은 무엇인가?

  A. class와 for를 사용하지 못한다. => 대신에 각각 className, htmlFor를 사용하면 된다.

- 웹팩을 사용해야 하는 이유는?

  A.

  - 유지보수성을 향상 시키기 위해
  - 스크립트 간 중복을 방지하기 위해
  - 간단하게 바벨 적용 가능
  - 쓸데 없는 코드 제거 가능 ex) console.log()를 다 제외시킬 수 있다.

- 웹팩이란?

  A. 여러 개의 자바스크립트 파일을 합쳐서 한번에 합쳐서 하나의 자바스크립트 파일로 만들어주는 것.

- 함수형 컴포넌트(Functional Component)에서 사용할 수 없었던 2가지는?

  A. setState()와 ref

- 바벨과 웹팩을 연결해주는 역할을 하는 것은?

  A. babel-loader



- 함수형 컴포넌트는 어떤 때에 쓰나?

  setState나 ref를 안쓰는 경우 쓴다.

- `const [value, setValue] = React.useState('');`에서 `value`와 `setValue`에 각각 어떤 것이 할당 되는가?

  - `React.useState()` 함수가 호출되고 나면 배열을 반환
  - 그 배열의 첫번째 원소는 상태 값이고, 두번째 원소는 상태를 설정하는 함수

- class보다 hooks를 썻을 때 장점과 단점은?

  - 장점 : 코드가 짦아지고 간결해진다.
  - 단점 : 리랜더링 될 때 함수 전체를 다시 실행하기 때문에 조금 더 느리다.

- node에서 제공하는 path로 지금 현재 경로를 가져오는 방법은?

  ```
    const path = require('path');
    path.join(__dirname, '');
  ```

- `npm run`과 동일하게 쓸 수 있는 명령어는?

  `npx`

