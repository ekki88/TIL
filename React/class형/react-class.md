※ 생활코딩 react강의(2019년) 수강 후 작성  <br/>

<b>클래스형 문법</b>
```
class App extends Component {
  render() {
    return(
      <div></div>
     );
   } 
} 
```
리액트의 컴포넌트를 상속해 app이라는 클래스만듦 <br/>
render 사용해야함 <br/>

---

props <br/>
컴포넌트의 속성을 표현할 수 있다. <br/>
컴포넌트를 조작할 수 있게 함 <br/>

state <br/>
컴포넌트 내부적으로 사용되는 것들 <br/>

---

props 사용시 문법 <br/>
```
class App extends Component {
  construtor(props){
    super(props);
    this.state = {
      //state초기화값
    }
  }  
  render() {
    return(
      <div></div>
     );
   } 
} 
```
render 함수보다 먼저 실행되면서 그 컴포넌트를 초기화 해주고싶은 코드는 construtor안에 작성<br/>
construtor 제일먼저 실행되서 초기화를 담당한다 <br/>

---
preventDefault <br/>
이벤트의 기본동작을 못하게 막는 것 <br/>

---

bind (this) <br/>
함수가 끝난 직후에 추가해주면 됨<br/>
this의 경우 못찾아서 bind함수 추가해주는거!<br/>
```
this.setState({});
```
state 변경하고 싶을 때
