### redux-middleware
리덕스가 지니고 있는 핵심기능 (context API, MobX와 차별된)<br/>

#### 액션-> 미들웨어 -> 리듀서-> 스토어
미들웨어 사용: 액션이 디스패치 된 다음, 리듀서에서 액션 받아와 업데이트 하기 전 <br/>

#### 추가적인 작업 가능
- 특정조건에 따라 액션이 무시되게
- 액션을 콘솔에 출력, 서버쪽에 로깅
- 액션이 디스패치됐을때 이를 수정해 리듀서 전달
- 특정액션이 발생했을때 이에 기반하여 다른액션 발생
- 특정액션이 발생했을때 특정 자바스크립트 함수 실행

->로깅: 어떤 소프트웨어가 실행할때 발생하는 이벤트를 추적하는 수단

<b>주된 사용용도는 비동기 작업을 처리 할 때 ! <br/>
  미들웨어 라이브러리 종류에는 redux-thunk, redux-saga, redux-observable, redux-promise-middeleware 등이 있다 </b>
  
