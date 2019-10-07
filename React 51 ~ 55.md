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





useReducer 는 어떠한 경우에 사용하는가?

- A.

------

다음 빈칸에 알맞은 코드를 쓰세요. (hint: rowData의 길이 만큼 배열과 관련된 함수)

```
<tr>
    {_____________________________((td, i) => ( 
        <Td key={i} dispatch={dispatch} rowIndex={rowIndex} cellIndex={i} cellData={rowData[i]} >{''}</Td>
    ))}
</tr>
```

- A.

------

dispatch 안에 있는 action을 하는 것은 [동기/비동기] 이다. component 자체를 기억하는 방법은 [memo/useMemo] 이다.

- A.



Q1. dispatch가 가지는 객체를 무엇이라 부르나

- A.

  action

Q2. state를 수정할때 reducer는 어떠한 역할을 하는가

- A.

  action이 어떤 수행을 할지 관리한다.

Q3. useReducer는 업데이트를 트리거 하는 컴포넌트의 성능을 최적화할 수 있는 이유는 콜백 대신      ``를 전달 할 수 있기 때문이다.

- A.

  dispatch, React는 dispatch 함수의 동일성이 안정적이고 리렌더링 시에도 변경되지 않으리라는 것을 보장합니다. 이것이 useEffect나 useCallback 의존성 목록에 이 함수를 포함하지 않아도 괜찮은 이유입니다.

- 1. 다음이 설명하는 Hook 메서드는 무엇인가?

> useState의 대체 함수이다. (state, action) => newState의 형태로 reducer을 받고 dispatch 메서드와 짝의 형태로 현재 state를 반환한다.

- 답

- 1. props로 전달하는 함수는 대부분 [  ]으로 감싸주는 것이 좋다. 함수 내부 데이터 중 바뀔 여지가 있는 것을 [   ] 의 두 번째 인자로 넣어준다.

  useCallback

- 1. useReducer 메서드를 사용하면 state는 직접 수정할 수 없고 state를 수정하고 싶으면 [ 1 ]을 만들고 실행해야 한다. 이벤트가 발생할 때 [ 1 ]을 [ 2 ]해서 state를 변경해야 한다. state를 어떻게 변경할지는 [ 3 ]에 기록한다.

  2. action 2. dispatch  3. reducer

     

- Q1. 규모가 큰 앱이라면 useReducer, contextAPI보다 Redux를 사용하게 된다. 이유는 무엇인가?

  비동기 부분 처리를 위해서 결국 리덕스를 사용해야 한다.

- Q2. useReducer 함수에 전달되는 3개의 인자를 순서대로 나열하시오.

  reducer, initialState, lazyInitialize(복잡해질 때에만 사용)

- Q3. 다음의 코드를 수정하시오.

  ```
    const reducer = (state, action) => {
    	switch (action.type) {
    		case 'SET_WINNER':
    			state.winner = action.winner;	// winner는 배열이다.
    	};
    };
  ```

  - 답

    ```
      const reducer = (state, action) => {
      	switch (action.type) {
      		case 'SET_WINNER':
      			return {
      				...state,
      				winner: action.winner,	
      			};
      	};
      };
    ```

1. useReducer란?

   - 답

     useState의 대체 함수, 리덕스에 개념을 따온 것으로 하나의 state와 하나의 setState로 만들어서 state 개수를 줄여서 상태관리를 하는것

2. useReducer를 쓸 때 상태를 변경하고 싶으면 어떻게 해야하나?

   - 답

     state를 수정하고 싶으면 이벤트가 실행될때 action을 dispatch(실행)해서 state를 변경해야한다.

3. OX 문제

   리덕스는 state가 비동기적으로 바뀌는데 useReducer에서 dispatch는 동기다. ( O / X )

   - 답

     X, 리덕스는 state가 동기적으로 바뀌는데 useRedcuer에서 dispatch는 비동기다.