### React-Hook-Form

```
npm install react-hook-form
```
💨 설치

```javascript

function Todo() {
  const {register, watch, handleSubmit, formState} = useForm();
  const onValid=(data: any)=>{
  console.log(data);
  }
  return(
    <div>
      <form onSubmit={handleSubmit(onValid)}>
        <input {...register("todo"), {required:true, minLength:10} } placeholder="hey"/>
      </form>
    </div>
  )
}

```
<b>register</b></br>
◾ name, onBlur, onChange, onClick, ref를 return하는 함수 ("대소문자,_ok 띄어쓰기x")</br>
<b>watch</b> </br>
◾ form의 입력값들의 변화를 관찰 할 수 있게 해주는 함수 </br>
<b>handleSubmit</b></br>
◾ input에 담긴 값들을 register에서 등록한 기준에 따라 validation </br>
◾ 추가적인 작업 가능 두개의 인자를 가짐 (데이터가 유효할 때, 데이터가 유효하지않을 때)</br>
<b>formState</b> </br>
◾ 에러확인
