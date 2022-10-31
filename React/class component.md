### - 클래스 기반 컴포넌트 
- state의 사용이 가능하여 상태저장이 가능
- 리액트 라이프사이클 메서드사용가능
-  클래스이기때문에 return문이 없고 render() 함수가 필수적으로 있어야 JSX반환 가능
- 함수형 컴포넌트보다 먼저 나왔기때문에 유지보수를 위해 알아둬야함

#### 사용
- 예약어 class입력
- import component
- render 반드시 사용
- 클래스를 만들고 extendscomponent로 확장
- props의 경우 this바인딩해서 사용

#### 상태정의
- 상태를 정의할때 constructor() 사용
- 클래스의 상태는 늘 객체
- 상태변경시 this.state 사용 
- super() 상위클래스 생성자 호출 

#### 라이프 사이클 메서드
- componentDidMount() = useEffect(.. ,[]) 의존성 배열 X
- componentDidUpdate() = useEffect(.. ,[]) 의존성 배열 O
- componentWillMount()= useEffect에 있는 cleanup 함수와 같음 
- effect함수가 다시 실행되기 직전에 호출되면 항상 컴포넌트가 DOM에서 삭제되기전에 호출
 
---


