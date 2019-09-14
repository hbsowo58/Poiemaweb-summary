바뀔 수 있는 부분은 state

Math.ceil(Math.random()*9) 랜덤값



(<div>/</div>) 코딩스타일



div{}곱하기{}는?/div 태그안에 {} 자바스크립트 사용가능



input.onchange = (e) => { console.log(e.target.value)} 콘솔에 입력값 계속출력

onSubmit={onSubmit} 값 제출



예전에는 쓸데없는 div가 필요했다(개선됨)  -> 빈태그 대체 <></>

-바벨이 처리못해줘서 <React.Fragement> 나중에 지원가능하면 빈태그 대체



(컨텐츠) 그룹연산자  = 있으나마나, 유의미한곳은 우선순위 높힐때

나는 미친 개발자다 (((())))



 

폼이 없으면 onClick 폼이있으면 onSubmit



함수를 따로뺏을때는 => 화살표함수를 사용해야함





약속) 예전값을 쓸때는 리턴을 사용하기로 !

setState 뒤에 return을 써서 (prevState)사용가능  =카운터예제



setState를 여러개쓰면 비동기라 



input에다 포커스를 주고싶다면? 



ref={(c) => {this.input =c;}}

변수 input 선언, (랜더위에) 



렌더링수

최초랜더링

setState바뀐만큼,

입력했을때 렌더링 => 나중에 랜더링이많아지면 (랜더링할때 10초걸리는게 있다면?)



따로빼는이유 랜더링이 새로 실행되므로 (setState될때마다) 함수가 계속생긴다.

그러므로 성능상 밖으로 빼는게 좋다





- Q. setState는 []이다

  A. 비동기

- Q. setState 메서드를 이용해 state를 변경시킬 때마다 []가 다시 실행된다

  A. render함수

- Q. ref는 언제 사용하는가?

  A. DOM요소에 직접 접근할 필요가 있을 때. 예) input 요소에 포커스

- Q. Class에서 메서드를 정의할 때 화살표함수를 사용하면 편리한데 그 이유는?

  A.함수 리터럴 사용 시 this 바인딩 이슈가 발생하기 때문에

- Q. 예전 State 값으로 새로운 State를 만들 때는 어떤걸 사용해야 할까?

  A. return을 해주는 함수를 사용하자.



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

