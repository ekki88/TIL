# class
#### ES6에 추가된 스펙
```JavaScript
class User2 {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  showName() {
    console.log(this.name);
  }
}

const tom = new User2('Tom', 19);
```
▶ class 키워드 사용 <br/>
▶ constructor: 객체를 만들어주는 생성자메서드 <br/>
▶ new를 통해 호출시 자동으로 실행됨, new 없으면 에러남 <br/>
▶ showName처럼 클래스 내에 정의된 메서드는 User2 프로토타입에 저장됨 <br/>

---

#### class 상속  
```JavaScript
class Car {
  constructor(color) {
    this.color = color;
    this.wheels = 4;
  }
  drive() {
    console.log("deive..");
  }
  stop() {
    console.log("stop!");
  }
}

class Bmw extends Car {
  prak() {
    console.log("PARK");
   }
}

const z4 = new Bmw("black");
```
▶ extends 키워드 사용 <br/>

---

#### 메소드 오버라이딩 (method overriding)
```JavaScript
class Car {
  constructor(color) {
    this.color = color;
    this.wheels = 4;
  }
  drive() {
    console.log("deive..");
  }
  stop() {
    console.log("stop!");
  }
}

class Bmw extends Car {
  prak() {
    console.log("PARK");
   }
  stop() {
    super.stop();
    console.log("off");
  }
}

const z4 = new Bmw("black");
```
▶ 동일한 이름으로 메소드정의시 덮어쓰게됨 <br/>
▶ 만약 부모에 있는 메소드로 하고싶다면 super키워드 사용하면 됨<br/>

---

#### 오버라이딩 (overriding)
```JavaScript
class Car {
    constructor(color) { //{}, this로 빈객체를 가르킴
      this.color = color;
      this.wheels = 4;
    }
    drive() {
      console.log("deive..");
    }
    stop() {
      console.log("stop!");
    }
  }
  
  class Bmw extends Car {
    constructor(color) {
      // super(color);
      this.navigation = 1;
    }
    prak() {
      console.log("PARK");
     }
  }
  
  const z4 = new Bmw("black");
```
▶ 부모생성자를 반드시 먼저 호출해야함<br/>
