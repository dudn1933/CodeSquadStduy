# getElementById 와 querySelector의 차이

> getElementById() 란 무엇인가?
```
const ID = document.getElementById(id);
```

태그에 붙여준 id 값을 통해 <code>element</code>를 반환한다. 만약 id값이 없다면 null을 <code>return</code>를 반환한다.</br></br>

> querySelector() 란 무엇인가?
```
const ID = document.querySelector(selectors);
```
selector의 구체적인 그룹과 일치하는 document안 첫번째 엘리먼트를 반환한다. 일치하는게 없으면 null반환한다. id이면 #을 class면 .을 붙여주어야 한다.

</br></br>

이제 둘을 비교해보자.
</br>

```
<form id="user">
    <input type="text" id="userID" placeholder="ID를 입력하세요"/>
</form>
```

이와 같은 코드가 있다고 가정해보자!
</br>
</br>

<code>getElementById</code>의 경우</br>

```
const userID = document.getElementById('userID')

위와 같이 id값으로 지정해준 값을 넣어주면 된다.
```

<code>querySelector</code>의 경우</br>

```
const userID = document.querySelecotr('#userID')

위와 같이 id값으로 지정해준 값에 id 값을 뜻하는 #을 붙여주어야 한다.
```

</br>

> querySelectorAll vs selectElementByClassName

```
<form id="productList">
  <input id="product1" class="product" type="text" />
  <input id="product2" class="product" type="text" />
  <input id="product3" class="product" type="text" />
</form>
```

<code>getElementByClassName</code>

```
const products = document.getElementsByClassName("product")
```

<code>querySelectorAll</code>

```
const products = document.querySelectorAll("#productList .product")
```

두개의 결과는 똑같다.</br>

그러나,</br>
<code>getElementsByClassName</code>은 <strong style="color:red;">HTMLCollection</strong>에 리턴이 되고 <code>querySelectorAll</code>은 <strong style="color:red;">NodeList</strong>에 리턴이 된다.

> HTMLcollection & NodeList 란 무엇인가??

HTMLCollection의 항목은 name, id 속성으로 접근이 가능하다.</br>
반면에, NodeList의 항목은 인덱스 번호로만 접근이 가능하다.