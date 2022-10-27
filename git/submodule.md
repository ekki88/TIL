### git submodule

- 저장소 안에 다른 저장소를 원하는 디렉토리에 복제하는 기능
- 스스로 저장소가 될수 있고 원하는 이름폴더에 존재
- 특정 버전과 디렉토리 연결 더 높은 버전 반영 준비가 되었을때 언제든지 쉽게 변경
- 개발에 필요한 모듈만 복제 -> 저장소가 작게 운영되는데 도움이 됨 

---

### 사용
```
git submodule add <submodule-url>
```
메인으로 사용하는 깃에서 서브모듈 사용하고싶다면 위 명령어 사용
```
git submodule init
```
서브모듈 정보를 기반으로 로컬 환경설정 파일을 만들어줌
```
git submodule update
```
디렉토리에 연결된 버전으로 Checkout
```
git submodule update --remote
```
디렉토리의 서브모듈 원격저장소에 최신버전으로 Checkout
```
git submodule update --remote -recursive
```
하위에 있는 모든 것을 동시에 업데이트 함 
```
git submodule foreach <명령>
```
일괄 명령 가능, 여러개의 명령을 하고싶다면 ";" 사용
```
git submodule init <사용하고싶은 모듈>
```
클론시 서브모듈은 안 가져와줌 명시적으로 클론해야함 <br/>
모든 서브모듈 가지고 오고싶으면 <사용하고싶은 모듈> 제외<br/>

---

#### .gitmodules
```
[submodule "폴더1"]
    path = 폴더1
    url = 깃주소
[submodule "폴더2"]
    path = 폴더2
    url = 깃주소
```
모든 서브모듈의 정보를 담고있음

#### .git/conpig
```
.git/conpig
```
내가 사용하는 서브모듈의 정보만 적혀있음

---

##### git remote -v
깃 저장소 주소 확인 
