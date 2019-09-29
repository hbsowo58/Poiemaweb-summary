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