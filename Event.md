# Event handler 과 Event listener

> handler

- 이벤트가 발생했을 때 그 처리를 담당하는 실행 함수를 가르킨다.
- 특정 요소에서 발생한 이벤트를 처리하기 위해서는 Eventhandler 라는 함수를 작성하여 연결해야만 한다.
- 이벤트 핸들러가 연결된 특정 요소에서 지정된 타입의 이벤트가 발생하면, 웹 브라우저는 이벤트 리스너에 연결된 에벤트 핸들러를 실행한다.
- 이벤트 핸들러 함수는 이벤트 객체를 인수로 전달받을 수 있다. 이렇게 전달받은 이벤트 객체를 이용하여 이벤트의 성질을 결정하거나, 이벤트의 기본 동작을 막을 수도 있다.

</br>

> listener

- 특정한 이벤트에 대해서 일어날 동작을 정의 할 수 있다.
- 지정된 타입의 이벤트가 특정 요소에서 발생하면, 웹 브라우저는 그 요소에 등록된 이벤트 리스너를 실행시킨다.
- 이벤트 리스너와 이벤트 핸들러를 합쳐서 이벤트 리스너라고 하기도 한다.

<table style="border: 1px solid; margin-left:20px;">
    <th style="text-align:center; border:1px solid;">이벤트</br>Event</th>
    <th style="text-align:center; border:1px solid;">이벤트 속성</th>
    <th style="text-align:center; border:1px solid;">이벤트 핸들러</br>Event handler</th>
    <tr>
    <td style="text-align:center; border:1px solid;">Click</td>
    <td style="text-align:center; border:1px solid;">onClick</td>
    <td style="text-align:center; border:1px solid;">function() {}</td>
    </tr>
</table>

</br>
</br>

다시한번 정리하면</br>
> Event handler

이벤트 핸들러는 <code>객체의 <strong>"Event handler"</strong> 속성을 사용하여 JavaScript</code>에서 인식 할 수 있다.

</br>

> Event listener

JavaScript에서 이벤트를 사용하는 다른 방법은 이벤트 리스너를 객체에 추가하는 것이다.</br></br>
객체에 이벤트 리스너를 추가하면 사용자 또는 브라우저에 의해 트리거되는 광범위한 이벤트를 포착할 수 있다.

</br>

## 차이점

button을 예시로

- 메서드인 이벤트 처리기를 사용하는 경우 차이점은 동일한 button 클릭에 대해 두 개의 이벤트 처리기를 추가하면 두 번째 이벤트 처리기가 첫 번째 이벤트를 덮어쓰고 해당 이벤트만 트리거 된다는 것이다.

> example

핸들러만 사용하는 경우
```
const button = document.querySelector(".btn")

button.onclick = () => {
    console.log("Hello!");
};

button.onclick = () => {
    console.log("How are you?");
};

output

How are you?
```

이렇게 하면 첫 번째 항목을 덮어쓰고 사용자가 버튼을 클릭하면 "How are you?"를 콘솔창에 나타낸다.

> addEventListener를 사용한다면?

```
const button = document.querySelector(".btn");

button.addEventListener("click", event => {
    console.log("Hello!");
});

button.addEventListener("click", event => {
    console.log("How are you?");
});

output

Hello!
How are you?
```
이 경우 사용자가 버튼을 클릭할 때 여러함수를 호출할 수 있다.
</br>

따라서 우리가 어떠한 이벤트를 추가해야 할 경우 미래에 내가 추가할 것이 있는가? 를 따져서 사용하면 되지만 처음부터 listener을 사용하면 이런걸 고민할 필요가 사라진다.</br>
따라서 나는 listener을 사용할 계획이다.