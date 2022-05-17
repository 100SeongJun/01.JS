# 객체와 배열

## [객체(Object)](https://github.com/100SeongJun/JS/blob/main/step05_object/object_lab01.html)

- 객체를 생성할 때 사용자 생성자 함수는 화살표 함수를 사요할 수 없다. (내부에 this를 사용할 수 없음)

- 존재하는 사물의 실체(설계도를 필요로 함)
- 리터럴 (코드상에서 데이터를 표현하는 방식)
- 생성자 함수

  - 함수 이름의 첫 글자는 대문자로 시작
  - new 연산자를 붙여 실행

- 사용자정의 생성자 함수

  - this를 사용하여 만들어질 객체를 참조

- Object

  - 모든 계체의 최상위, prototype은 객체의 설계도
  - 모든 객체는 Object의 prototype을 통해 객체의 정보를 사용하고있다.
  - 모든 객체는 Object를 상속하고 있다.

- instanceof
  - 좌측이 우측을 통해 만들어졌는지(상속받았는지) 확인 (A instanceof B)

---

## [배열](https://github.com/100SeongJun/JS/blob/main/step05_object/array_lab02.html)

<br>

|이름|명령어|설명|
|:------:|:-----------------------------: | :--------: |
|조회|arr[index]|배열의index번호에 대한 요소 조회|
|조회2|arr[arr.length-1]|배열의 마지막 요소 조회|
|길이|arr.length|배열의 크기 출력|
|추가|arr.push(7,8)|요소 삽입|
|추가2|arr.unshift(0,1)|배열의 맨 앞 요소 추가|
|삭제|arr.pop()|맨 뒤 요소 삭제(+반환)|
|삭제2|arr.shift()|맨 앞 요소 삭제(+반환)|
|삭제3|arr.splice(idx1,n,m)|지정한 인덱스의 요소 포함 n개 제거, m추가|
|범위지정|arr.slice(idx1,idx2)|배열의 특정범위 지정(idx1 < idx2조건 성립 시)|
|인덱스값 변환|arr.indexOf(n)|배열의 n 요소의 idx값 반환(없으면 -1 반환)|

- 유사배열
  - 순차적으로 내부 요소에 접근할 수 있는 이터러블(배열의 일반화)한 객체만 사용가능
  - Array.from() 유사 배열을 받아 진짜 배열로 변환

```javascript
let likeArray = {
    0:'오늘 점심',
    1:'뭐먹지',
    length:2
}  
```

- Join()
  - 배열에 대한 요소 묶음

- foreach()
  - 요소를 하나씩 모두 넘김 / 배열만 사용 가능한 메서드

- map()
  - 요소를 하나씩 모두 넘김

```javascript
  let infom = info.map(info => info.name);
  
```

- filter()

```javascript
console.log(todos.filter(todo => todo.done===true));
// 결과값을 배열로 돌려줌
```

---

## [문자열](https://github.com/100SeongJun/JS/blob/main/step05_object/string_lab03.html)

|명령어|설명|
|:----:|:-----:|
|charAt(idx)|해당 위치 인덱스의 문자 변환|
|substring(idx1,idx2)|idx1부터 idx2 - 1 까지의 문자 반환|
|replace(바꾸려는 글자,바꿀 글자)|해당 글자를 원하는 글자로 변경|
|split('')|기준에 따라 문자열을 분할하여 배열로 변환|
|concat()|문자열 결합|
---

## [숫자타입변환](https://github.com/100SeongJun/JS/blob/main/step05_object/number_lab04.html)

|명령어|설명|
|:-------:|:-------:|
|Number(value)|문자열 숫자로 변환|
|parseInt(value)| 소수점을 제외하고 정수로 반환(버림)|
|parseFloat(value)|소수까지 모두 출력|
|Value.toFixed(n)|n 자리까지 남김|
---

## [날짜](https://github.com/100SeongJun/JS/blob/main/step05_object/date_lab05.html)

|메서드|설명|
|:-------:|:-------:|
|getFullYear()|년 출력|
|getMonth()| 달 출력(-1 해줘야 원래 값)|
|getDate()|일 출력|
|getDay()|요일 출력(0:일요일)|
|getHours()|시간 출력|
|getMinutes()|분 출력|
|getSeconds()|초 출력|
