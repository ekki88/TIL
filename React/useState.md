# useState
#### 📌변경이 가능한 값을 리턴, 그리고 값을 업데이트 할 수 있는 함수를 리턴한다

```javascript
const [num, setNum] = useState(0);

<button onClick={()=> {
  setNum(num + 1)//1 
  setNum(num + 1)//1
  setNum(num + 1)//1
  
  // 기본값이 계속 찍히기 때문에 몇번을 반복해도 1 
  
  setNum((prev)=> prev + 1)//1
  setNum((prev)=> prev + 1)//2
  setNum((prev)=> prev + 1)//3
  
  // 이전값에서 더해지기때문에 수가 올라감, 이전 상태값 콜백으로 사용 할 수 있음
  
}}

```
