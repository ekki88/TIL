### Object.assign
assign()메서드는 두번째 매개변수 객체의 프로퍼치를 복사하여 첫번째 매개변수 객체의 프로퍼티에 추가한 뒤 첫번째 매개변수 객체를 반환하는 메서드<br/>

-> 왜 사용하나요?
원본 데이터는 그대로 두고 복사본으로 어떤 작업을 수행하기 위해<br/>

---
### 사용
```
Object.assign(target, ...sources) 
```
첫 번째 파라미터 : 모든 객체가 합쳐서 모여지게 될 객체.<br/>
두 번째부터 마지막 파라미터 : 첫 번째 파라미터로 합쳐질 객체.<br/>
