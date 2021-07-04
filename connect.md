# Connect

### connect([mapStateToProps], [mapDispatchToProps], [mergeProps], [options])

connect는 react-redux의 API 입니다. 이 함수는 컴포넌트를 store에 연결해 줍니다.

connect 함수는 특정 컴포넌트 클래스의 props를 store에 연결시켜주는 함수를 리턴합니다. 리턴된 함수에 컴포넌트를 인수로 넣어주면 기존 컴포넌트가 수정되는 것이 아니라 새로운 컴포는터를 리턴합니다.

### connect의 parameter

mapStateToProps(state, [ownProps]) : store의 state를 컴포넌트의 props에 매핑 시켜줍니다. ownProps 인자가 명시될 경우, 이를 통해 함수 내부에서 컴포넌트의 props 값에 접근 할 수 있습니다. 즉, store.state를 props로 접근 할 수 있도록 합니다.

mapDispatchToPRops(dispatch, [ownProps]) : 컴포넌트의 함수형 props를 실행 했을 때, 개발자가 지정한 action을 dispatch 하도록 설정합니다. ownProps 는 동일 합니다. 즉, props._function_을 통해 action을 dispatch 할 수 있도록 합니다.
