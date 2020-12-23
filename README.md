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
<img src="https://i.ibb.co/b7v30tM/callback.jpg">
코드의 실행결과는 이렇게 나오게 된다.
<img src="https://i.ibb.co/hCL7pjZ/callback2.jpg">
이미지의 우측 call stack을 보게되면 zero -> one -> two -> three -> console.log가 실행되는 것을 볼 수 있다.
그리고 다음 과정을 실행하면 three함수까지 전부 실행 되었기 때문에 스택에서 three -> two -> one -> zero 순으로 제거된다.

### Step Over
- blackpoint의 다음 라인으로 이동한다. 이때 다음 라인이 함수라면 함수를 실행하되 내부로 들어가지 않는다.
<img src="https://i.ibb.co/7gNbvQd/StepOver.jpg">

### Step Into
- blackpoint의 다음 라인으로 이동한다. 이때 다음 라인이 함수라면 함수 내부로 들어간다.
<img src="https://i.ibb.co/2ZHGQLx/StepInto.jpg">

### Step Out
- 현재 함수의 리턴으로 이동한다. 즉 현재 함수를 빠져나온다.
<img src="https://i.ibb.co/whVSYt8/StepOut.jpg">