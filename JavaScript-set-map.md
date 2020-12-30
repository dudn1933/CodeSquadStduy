JavaScript-set-map
==================
### set란?
 - set은 중복을 허용하지 않는 데이터 집합이다.
 - add를 통해 value를 추가할 수 있고 delete를 통해 삭제도 가능하다.
 # set의 메서드
 - has(key) = 해당 요소의 존재여부를 파악하여 Boolean 값으로 반환한다.
 - keys() = 삽입순으로 요소의 값 나열한다.
 - values() = 요소의 value값을 나열한다.
 - add(value) = 값을 추가한다.
 - clear() = Set의 모든 요소를 제거한다
 - delete(value) = 매개변수로 지정한 값을 제거한다.
 - entries() = 모든 요소를 key, value 형태로 반환한다.
 

### Map이란?
 - map는 함수, 객체등도 key 값으로 넣을 수 있다.
 - set을 통해 key, value 형식으로 값을 추가하거나 변경할 수 있다.
 - get을 통해 값으로 접근하거나 has를 통해 값의 존재 여부를 파악할 수 있다.
 - size를 통해 map이 가지고 있는 요소의 갯수를 파악할 수 있다.
 # map의 메서드
 - get(key) = 매개변수로 지정한 key의 value를 반환, 없으면 undefined
 - has(key) = 해당 요소의 존재여부를 파악하여 Boolean 값으로 반환한다.
 - keys() = 요소의 키값을 나열한다.
 - values() = 요소의 value값을 나열한다.
 - set(key, value) = key와 value값을 추가하거나 변경한다.
 - clear() = map의 모든 요소를 제거한다.
 - delete(key) = 지정한 key와 value를 제거한다.
 - entries() = 모든 요소를 key, value 형태로 반환한다.