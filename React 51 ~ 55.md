useReducer는 useState와 비슷하게 동작한다 (O/X)

O

*const [state, dispatch] = useReducer(reducer, initialArg, init);* 역할

useReucer는 초기 state를 받고 반영될 State와 Dispatch를 반환



useReducer에 contextAPI까지 사용하면 redux를 대체할 수 있다(O/X)

소규모 대체가능하다, 그러다 비동기 부분때문에 리덕스를 사용해야된다





useReducer - redux의 핵심부분을 가져옴 state들이 많아지면 

contextApi를 까지 쓰면 redux 대체가능? 소규모 대체가능 



결국 비동기 부분 처리를 위해 리덕스를 써야된다.



react 성능최적화 = 컴포넌트별로 쪼갤 수 록 좋다



useReducer(reducer, initialState, 3번째인자 잘안씀)



useReducer 단점 : 객체를 얕은 복사해야되는데 immer라는 라이브러리로 가독성 해결



부모 - 자식 구조가 10개면 10번 넘겨주어야 하는데 이걸 context Api 사용



useReducer의 state는 비동기적으로 바뀜(dispatch)



성능최적화 이칸만 클릭했는데 전체가 바뀜 