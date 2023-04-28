### add
✔️ 작업 디렉토리(working directory) 상의 변경 내용을 스테이징 영역(staging area)에 추가하기 위해서 사용<br/>
```
git add .
```
파일 전체

```
git add <file> 
```
특정파일만 add 하고 싶을 때
<br/>
<br/>
### restore
✔️ add한 파일을 되돌리고싶을때 사용
```
git reset HEAD <file> 
```
전체 취소
```
git reset HEAD <file> 
```
특정파일 취소
<br/>
<br/>
### merge
✔️ git branch를 다른 branch와 합치는 과정
```
git merge <대상브랜치>
```

```
<<<<<<<<<<<<<<<<<<<HEAD
[현재 브랜치의 변경사항]
===================구분선
[머지 대상 브랜치의 변경사항]
>>>>>>>>>>>>>>>>>>>대상 브랜치명
```
CONFLICT 컨플릭 발생(충돌 일어났을 때)
<<,==,>>를 모두 없애고 원하는 변경사항 반영하면 됨
