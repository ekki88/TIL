# React class

### props
부모컴포넌트가 자식컴포넌트에게 주는 값 <br/>
자식컴포넌트에서 props를 받기오기만하고 직접 수정할 수 없음 <br/>


### state
컴포넌트 내부에서 선언하며 내부에서 값 변경 가능

#### 클래스 형 컴포넌트에서 state 기본 사용법

```
import React, {Component} from 'react'

class Counter extends Component {
    //컴포넌트에서 state를 설정할 때는 다음과 같이
    //constructor 메서드를 작성하여 설정한다. 
    //constructor는 클래스형 컴포넌트의 생성자 메서드인데,
    //이 때 반드시 super(props)를 호출해 주어야 한다. 
    constructor(props) {
        //현재 클래스형 컴포넌트가 상속받고 있는 
        //리액트의 Component 클래스가 지닌 생성자 함수를 호출해 준다.
        super(props);
        //state의 초깃값 설정하기 
        this.state = {
            increaseNum : 0,
            decreaseNum : 100
        };
    }

    render(){
        //state를 조회할 때는 this.state로 조회한다. 
        const {increaseNum, decreaseNum} = this.state;
        return(
            <div>
                <h1>증가하는 값 : {increaseNum}</h1>
                <h2>감소하는 값 : {decreaseNum}</h2>
                <button
                    onClick={()=>{
                        //this.setState를 사용하여
                        //state에 새로운 값을 넣을 수 있다. 
                        this.setState({
                            increaseNum : increaseNum + 1,
                            decreaseNum : decreaseNum - 1
                        });
                    }}
                >
                    Increase / Decrease
                </button>
            </div>
        );
    }
}

export default Counter;
```
