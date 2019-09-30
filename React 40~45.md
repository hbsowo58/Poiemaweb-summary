리액트에서 자주사용하는 패턴 메소드 안에서 함수를 호출하는 부분을 



함수 정의하는 부분에 화살표룰 추가 () => () => 화살표를 연달아 쓰는 (고차함수)



Hooks는 라이프 사이클이 있지는 않지만 흉내를 낼 수 있다

=useEffect 함수컴포넌트 안에 작성



useEffect(()=>{

 return ()=> {

}

},[]);



마지막에 빈배열넣어두기 componentDidMount, componentDidUpdate 역할(1대1 대응은 아님)

return문 안이 componentWillUnmount 역할



두번째 배열에 인수를 넣어야 제대로동작 (이전에 클로져문제 해결)



함수컴포넌트는 렌더링이 될때마다  모든부분이 실행된다



setInterval 켜졌다가, 꺼졌다가 반복



'일단은 패턴처럼 외워두기'

[]안에가 비어있으면, 뭐가 바뀌어도 신경쓰지 않겠다



useEffect 여러번 사용가능, 배열에는 꼭 useEffect를 다시 실행할 값만 넣기



react.memo()로 감싸줘야 리 랜더링이 되지 않는다



useLayoutEffect(정말 특별한 경우에만 사용)

레이아웃의 변화를 감지할때 (화면이 바뀌기 전에)

useEffect(화면이 바뀌고 난후)

​												result , imgCoord, score

componentDidMount

componentDidUpdate

componentWillUnmount

 



class에선 라이프사이클 가로, Hooks에선 세로라고 생각



class에선 



componentDidMount(){

}



useEffect(()=>{})

useEffect(()=>{})

useEffect(()=>{})



클래스에선 한개에 세가지를 다, useEffect 1~3개씩 3번





로또추첨기 컴포넌트

usecall usememo



로또추첨기에서 번호 출력하는것도 꾀 많은 것을 잡아먹기때문에 랜더하는 부분 밖에 빼두기



대부분의 게임들이 미리 데이터를 미리 뽑아두고, 천천히 보여주는식의 방법을 사용한다

반복문을 기점으로 컴포넌트 분리

purecomponent memo로 감싸기 컴포넌트를 컴포넌트로 감싼것 (high order component)







- 리액트에서 많이 사용되는 패턴인, 메소드안에서 함수를 호출하는 부분 () ⇒ () ⇒  무엇이라고 하는가?

  고차함수

- Hooks에는 라이프사이클이 없다 (  O / X )

  O 없다. 하지만 흉내 낼 수 있다.

- useEffect의 마지막 배열은 어떤 라이프 사이클과 대응되는가?

  componentDidMount, componentDidUpdate

- useLayoutEffect 언제사용되는가?

  레이아웃의 변화를 감지할때 (화면이 바뀌기 전에)

- high ( order ) component란?

  컴포넌트를 컴포넌트로 감싼것