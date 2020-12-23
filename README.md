CodeSquadStduy
==============

### breakpoints란? 
- breakpoint는  console.log() 메서드보다 더 빠르게 버그를 찾고 수정하는 데 도움을 준다.
- 내가 지정한 범위까지 코드를 실행시켜 오류를 찾을때 유용하게 사용할 수 있다.

### watch사용법
- 만약 내가 함수에서 return값을 보고싶을때 watch에 return값을 적게되면 그 값을 보여준다.

### call stack의 의미
- call stack는 실행할 함수를 차곡차곡 쌓는 역할을 한다.
즉 call stack는 현재 어떤 함수가 동작하고 있는지, 그 함수 내에서 어떤 함수가 동작하는지, 다음에 어떤 함수가 호출되어야 하는지 등을 제어한다.
이 구문을 통해 확인할 수 있다.
<img src ="https://i.ibb.co/b7v30tM/callback.jpg">
코드의 실행결과는 이렇게 나오게 된다.
<img src ="https://i.ibb.co/hCL7pjZ/callback2.jpg">
따라서
