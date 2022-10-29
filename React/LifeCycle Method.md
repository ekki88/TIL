### 생명주기 메서드
클래스형 컴포넌트에서만 사용가능<br/>

---
#### 마운트
마운트될 때 발생하는 생명주기
- constructor
- getDerivedStateFromProps
- render
- componentDidMount

##### constructor
- constructor()는 컴포넌트의 생성자 메서드
- 컴포넌트가 만들어지면 가장 먼저 실행되는 메서드
- 생성자로 props를 전달받아 state를 초기화 해야 할 때 사용하는 메서드
- state를 초기화하지않는다면 구현하지않아도 됨
- 반드시 첫줄에 super(props);를 호출해야하며 그렇지 않은 경우 오류 발생
- constructor() 내부에서는 setState()메서드를 지원하지않음
```
constructor(props) {
	super(props);
	console.log("constructor");
}
```
##### getDerivedStateFromProps
- getDerivedStateFromProps는 props로 받아온 것을 state에 넣어주고 싶을 때 사용
- 앞에 static 필요, 이 안에서 this조회 할 수 없음
- 컴포넌트가 처음 렌더링 되기전에도 호출, 리렌더링 되기전에도 매번 실행 
- static 메서드이기때문에 this를 통해 컴포넌트에 접근 할 수 없음
- null 반환시 아무것도 갱신하지않음
* static메서드란?
##### render
- 컴포넌트를 렌더링하는 메서드
- 화면에 출력할 내용을 생성하여 반환
- prpos와 state 값으로만 생성해야함
- Side-Effect를 발생시켜서는 안됨
##### componentDidMount
- 컴포넌트의 첫번째 렌더링이 마치고나면 호출되는 메서드 (이 메서드가 호출되는 시점에는 화면에 컴포넌트 나타난 상태)
- DOM의 속성을 읽거나 직접 변경하는 작업 진행
- render()의 반환 값이 DOM에 반영된 후 호출됨
- 컴포넌트가 DOM에 반영된 시점이므로 DOM으로부터 필요정보 조회가능
- setState() 메서드 호출과 Side-Effect 코드 실행 가능

---
#### 업데이트
컴포넌트가 업데이트 되는 시점에 호출되는 생명주기 메서드들 <br/>
- getDerivedStateFromProps
- shouldComponentUpdate
- render
- getSnapshotBeforeUpdate
- componentDidUpdate

##### shouldComponentUpdate
- 컴포넌트가 리렌더링 할지 말지 결정하는 메서드
- 주로 최적화시 사용
##### getSnapshotBeforeUpdate
- 컴포넌트에 변화가 일어나기 직전의 DOM상태를 가져와 특정값을 반환,
- 그다음 발행하게 되는 getSnapshotBeforeUpdate 함수에서 받아와 사용 할 수 있음
- render()의 결과가 DOM에 반영되기 직전에 호출 됨
- 이전 DOM의 정보를 조회할 수 있는 메서드
- 이 메서드가 반환하는 값은 componentDidUpdate(prevProps, prevState, snapshot)의 세번째 인자에 전달됨
- 함수형컴포넌트+hook으로 대체 할 수 있는 기능 아직은 없음
##### componentDidUpdate
- 리렌더링마치고, 화면에 변화 모두 반영되고난뒤 호출되는 메서드
- 3번째 파라미터로 getSnapshotBeforeUpdate에서 반환한 값 조회 가능 
- Side-Effect 코드, setState()를 호출 할 수 있음
- 이전 prop, state를 전달받으므로 변경사항을 직접 비교할 수 있음

---
#### 언마운트
컴포넌트가 화면에서 사라지는것 
- componentWillUnmount

##### componentWillUnmount
- 외부라이브러리를 사용한게 있고 해당 라이브러리에 dispose기능이 있다면 호출 
- 컴포넌트 소멸 시 호출되는 유일한 메서드
- 이벤트 해제, 리소스 해제 등 소멸자로서의 역할

---
##### componentDidCatch(error, info)
- 첫번째 파라미터는 에러의 내용, 두번째 파라미터에서는 에러가 발생한 위치 알려줌
- 자식 컴포넌트에서 오류가 발생했을 때 호출 (자신의 오류는 잡아낼 수 없음)
- 매개변수 error는 오류객체, info는 오류를 발생시킨 componentStatck 정보를 포함하는 객체
- Commit 단계에서 호출되기 때문에 setState()와 Side-Effect 실행 가능
- (setState()를 호출하여 UI가 다시 렌더링 되도록 할 수 있지만 추후 릴리즈에서 막힐 예정이므로, 대신 getDerivedStateFromError()를 사용해야함)

```
defaultProps : props를 따로 지정해주지 않아도 기본값으로 전달 해주는 props
```
