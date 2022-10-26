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
사용시 styled.html태그 그리고 백틱사용<br/>
백틱 사이에 들어가는 부분은 CSS여야함<br/>

---
#### props 사용
```
const Box = styled.div`
    background-color: ${(props) => props.bgColor};
    width: 100px;
    height: 100px;
`;

function App() {
    return(
    <Main>
        <Box bgColor="pink" />
        <Box bgColor="blue" />
    </Main>
    )
}
```
흡사한 조건인데 일부 다를 때
(bgColor 사용하고 싶은 이름 사용)

---
#### 확장
```
const Box = styled.div`
    background-color: ${(props) => props.bgColor};
    width: 100px;
    height: 100px;
`;

const Circle = styled(Box)`
    border-radius: 50px;
`;

function App() {
    return(
    <Main>
        <Box bgColor="pink" />
        <Circle bgColor="blue" />
    </Main>
    )
}
```
기존 컴포넌트의 모든 속성을 들고와서 복붙하고 새로운 속성까지 더해 줌 <br/>
(Box의 모든 속성들을 들고 온 다음 Circle에 더해줌)
