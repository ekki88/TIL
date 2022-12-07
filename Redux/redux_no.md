# Redux
### store, reducer
```javascript
const reducer = () => {
  return "hello';
}; 

const store = createStore(reducer);

console.log(countStore.getState()); //hello
```
1)store(data저장하는 곳)를 만든다 = 스토어를 만들면 reducer를 만들어주길 요구<br/>
2️)reducer를 만든다 = 리듀서는? function(함수)여야하고, 오직 reducer만이 data를 modify <br/>
##### ▶ reducer가 return하는 건 application의 state가 됨<br/>

---

### action
```javascript
const reducer = (count = 0, action) => {
  return count;
}; 

const store = createStore(reducer);

countStore.dispatch({ type: "ADD" });
```
action redux에서 function을 부를때 쓰는 두번째 parameter,argument<br/>
action은 무조건 object여야함<br/>
##### ▶ reducer와 소통할 수 있는 <br/>

---
### subscribe
```javascript
import {createStore} from "redux";

const add = document.getElementById('add');
const minus = document.getElementById('minus');
const number = document.querySelector('number');

const reducer = (count, action) => {
  if (action.type === "ADD") {
    return count + 1;
  } else if (action.type === "MIUNS") {
    return count - 1;
  } else {
    return count;
  } 
};

const countStore = createStore(reducer); 

const handleAdd = () => {
  countStore.dispatch({ type: "ADD"})
}

const hadleMinus = () => {
  countStore.dispatch({ type: "MINUS"})
}

add.addEventListener("click",handleAdd);
minus.addEventListener("click", hadleMinus);
```
subscribe store안에 있는 변화를 알 수 있게 해줌<br/>
