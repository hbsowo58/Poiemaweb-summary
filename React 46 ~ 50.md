react의 장점 , jquery처럼 dom을 직접적으로 건들이지 않았다



componentDidUpdate() 조건문으로 해서 판단을 해준다

어떤게 바뀌었는지 판단할 수 있다  업데이트 하고 싶은 상황을 처리



라이프사이클을 처음할때는 console로 찍어보기



componetDidUpdate 잘못쓰면 재앙일어날 수 있음



memo나 purecomponent를 자식에 넣어줘야 불필요한 렌더링을 줄일 수 있음



[] componentDidMount

[xxx] componentDidUpdate 둘다 수행

캐싱 =기억해두기 useMemo 다시실행되지 않게



useMemo(()=> getWinNumbers(), []);

다시실행 x 

useMemo : 복잡한 함수 결괏값을 기억

useRef : 일반 값을 기억



useMemo(함수의 리턴값 기억) <-> useCallback (함수 자체를 기억)



모든 함수를 useCallback으로 감싸면, useMemo를 사용할 필요가 없을 것 같다. 그럼에도 useMemo가

필요한 이유



useCallback의 기본값은 빈배열이고, 바뀌는 state를 배열에 넣어주지않으면

최초의 것을 '계속' 기억하고 있는다



자식컴포넌트에 함수를 넘길때는 useCallback을 사용해야한다 (없으면 매번 새로운 함수가 

생성되기 때문에, 부모컴포넌트로부터 계속 새로운함수가 보내지면 부모가 계속 새로운 props를 준다고 판단해서 자식컴포넌트가 계속 리렌더링한다)



조건문 안에 hooks실행, (문제발생)  -> 함수,반복문 안에 넣지말기





















