#### ✅ provider 컴포넌트
```javascript
ReactDOM.render(
  <Provider store={store}
    <App />
  </Provider>
, document.getElementById('root'));
)
```
provider로 react컴포넌트 감싸줌 <br/>
-> 하위컴포넌트들이 provider를 통해 redux의 store에 접근할 수 있게 해줌 <br/>
provider에 store 줘서 접근권한을 줌 <br/>

---
#### ✅ connect 함수
```javascript
connect (mapStateToProps, mapDispatchToProps)(store와 연결시킬 컴포넌트);
```
컴포넌트를 store에 연결시키기 위해 사용 <br/>
(state는 store에 저장되어있음)

---
#### ✅ mapStateToProps
```javascript
function mapStateToProps(state, ownProps) {
  return {
    //객체여야함
  }
}
```
store로부터 데이터를 가져와 컴포넌트의 props에 넣음<br/>
첫번째 인자 state: store로부터 온 state<br/>
두번째 인자 ownProps: 생략가능, 컴포넌트가 현재 가지고 있는 props 보여줌<br/>
<br/>
#### ✅ mapDispatchToProps
```javascript
function mapDispatchToProps (dispatch, ownProps) {
}

//첫번째 인자 사용안하면 null
connect (null, mapDispatchToProps)(store와 연결시킬 컴포넌트);
```
컴포넌트 내에서 dispatch 사용 할 수 있게 해줌 <br/>
첫번째 인자 dispatch: redux의 store.dispatch()와 같음 <br/>
두번째 인자 ownProps: 생략가능, 컴포넌트가 현재 가지고 있는 props 보여줌 <br/>
