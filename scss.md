## SCSS란?

SCSS는 CSS의 상위집합으로서, CSS와 동일한 문법으로 SASS의 특별한 기능들이 추가되어 있는 것이다.

### Variable (변수)

CSS에 변수 개념을 도입하였다.
변수로 사용 가능한 형태는 숫자, 문자열, 폰트, 색상, null, lists, maps 가 있다.

변수를 사용할 때는 <code>$</code>문자를 사용한다.
```
ex => $width: 100px;
```

전역변수를 설정할 때는 <code>!global</code> 플래그를 사용한다.

### SCSS의 장점

선언을 중첩시킬 수 있다! 

다음의 코드를 보자.
```
/* CSS */

.container {
    width: 100%;
}

.container h1 {
    color: red;
}
```
일반 CSS에선 특정 선택자 안의 선택자를 스타일링 하려면 이렇게 코드를 작성해야 했다.

하지만, 이렇게 코드를 작성하다 보면 CSS가 길어질 경우 유지보수가 어려워지게 된다.

다음 코드를 보자.
```
/* SCSS */

.container {
    width: 100%;
    h1 {
        color: red;
    }
}
```
SCSS를 사용하면 이러한 장점을 가질 수 있어 좀 더 원활한 유지보수가 가능하다.

### 부모 선택자 리퍼런스

```
/ * SCSS */

a {
    color: black;
    &:hover {
        text-decoration: underline;
        color: gray;
    }
    &:visited {
        color: purple;
    }
}

비교구문 
/* CSS */

a {
    color: black;
}
a:hover {
    text-decoration: underline;
    color: gray;
}
a:visited {
    color: purple;
}
```

### Extend(상속)

```
.box {
    border: 1px solid gray;
    padding: 10px;
    display: inline-block;
}

.success-box {
    @extend .box;
    border: 1px solid green;
}
```
위와 같이 <code>@extend .box</code>로 box의 style를 상속 받을 수 있다.

### Mixin

Mixin은 SCSS의 아주 유용한 기능 중 하나인데, extend와 비슷하지만 argument(인수)를 받을 수 있다.

```
@mixin headline ($color, $size) {
    color: $color;
    font-size: $size;
}

h1 {
    @include headline(green, 12px);
}
```