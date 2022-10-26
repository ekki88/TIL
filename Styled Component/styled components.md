## Styled Componets
#### 설치
```
npm i styled-components
```

---
#### 사용

```
import styled from "styled-components"

const Main = styled.div`
    display:flex;
`;
const BoxOne = styled.div`
    background-color: pink;
    width: 100px;
    height: 100px;
`;
const BoxTwo = styled.div`
    background-color: blue;
    width: 100px;
    height: 100px;
`;

function App() {
    return(
    <Main>
        <BoxOwn />
        <BoxTwo />
    </Main>
    )
}
```
사용시 styled.html태그 그리고 백틱사용
백틱 사이에 들어가는 부분은 CSS여야함
