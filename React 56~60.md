리덕스 (동기적)

useReducer(비동기적)



context API (부모 거쳐서 받는게아니라 바로받을 수 있음)

TableContext.Provider value ={{ tableData: state.tableData, dispatch}} 넘길데이터 ,디스패치

 아래 컴포넌트에서 데이터에 접근할 수있음



성능 최적화 하기가 힘들다(객체가 새로생긴다) useMemo를 통해 캐싱을 한번해줘야

성능이 떨어지지 않는다



Context 는 `createContext` 라는 함수를 사용해서 만든다

함수를 호출하면 Provider 와 Consumer 라는 컴포넌트들이 반환됩니다. Provider 는 Context 에서 사용 할 값을 설정할 때 사용되고, Consumer 는 나중에 우리가 설정한 값을 불러와야 할 때 사용됩니다.



Context 를 언제 사용할까?

리액트의 트리구조에서 깊이가 깊어지는 컴포넌트 구조에서 상태를 관리할때





