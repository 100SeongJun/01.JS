# 비동기통신

## [비구조화 문법](https://github.com/100SeongJun/JS/blob/main/step07_apply/apply_lab01.html)

### 1. 삼항연산자

```javascript
  조건 ? true : false
  console.log(!false); // true
  console.log(!undefined);  //true
  ...
```

### 2. 논리 연산자

- || (or연산자)
  - or연산의 경우 앞이 true이면 뒤에 값 무시
  - 어떠한 조건이 뒤에 나와도 무조건 true이기 때문
- && (and 연산자)
  - and연산의 경우 앞이 false이면 뒤에 값 무시
  - 어떠한 조건이 뒤에 나와도 무조건 false이기 때문

### 3. 함수

- 파라미터 : 함수를 정의할 때 사용되는 소괄호 안의 변수값
- 인자 : 함수가 호출될 때 값을 넘겨주는 변수값

### 4. 비구조화 문법

```javascript
  // 객체
  const obj = {a:1,b:2};
  const {a,b} = obj;
  console.log(a); //1
  console.log(b); //2

  // 배열
  let arr2 = [1,2];
  let [one,two] = arr2;
  ...
```

- spread

    ```javascript
      let arr3=[1,2,6];
      let arr4=[...arr3,5];
    ```

- rest

    ```javascript
    let city = {
              continent: 'Asia',
              country_name: 'ROK',
              region: 'Busan'
          };

          let { region, ...country} = city;
    ```

- 상속

```javascript
  Child.prototype=Parent.prototype; //prototype 상속
  Child.prototype = {...Parent.prototype}; //spread 상속
  Child.prototype = Object.create(Parent.prototype); //가장 적절한 방법의 상속
  console.log(p3.__proto__.constructor); //누구로부터 만들어진 객체인지 확인 (상속 후 check 거의 필수)
```

## [JSON](https://github.com/100SeongJun/JS/blob/main/step07_apply/json_lab02.html)

- JavaScript Object Notation
  - 문자열의 형태로 데이터를 주고 받는 포맷
  - 내장 객체(js가 운여되는 전역으로 접근 가능)
  - key : value 한 쌍으로 구성, ""(큰따옴표)가 붙어 있는 상태

- JSON.stringfy(obj) : 객체를 JSON으로 변경(직렬화)
  - (객체, 배열, 문자형, 숫자형, boolean(true/false), null) 적용 가능
  - ! 함수, 심볼, undefined는 적용 안됨

- JSON.parse(obj) : JSON을 객체로 변경(역직렬화)

## [비동기통신](https://github.com/100SeongJun/JS/blob/main/step07_apply/asynchronous_lab03.html)

- JS는 인터프리터 형식으로 순차적으로 진행됨
- 동기 (synchronous): 요청 결과 응답 후 다음 동작이 실행되는 방식
- 비동기(asynchronous) : 요청 결과 응답과 별개로 다음 동작이 실행되는 방식
- 서버로부터 데이터 세팅, 문제 발생 시 별도로 실행되어야 하는 경우 필요

- CALLBACK Fnc : 함수의 매개변수로 전달되는 함수
- Promise : 전역객체(new 안됨)
  - 문법
    - resolve : new 연산자로 프로미스 객체 생성 가능
    - reject : 객체 생성 시 실행자 함수를 인자로 받아 실행
  - 프로미스는 진행되는 시점에 따라 상태값을 가짐
  - 실행자 함수의 종류는 2가지
    - resolve(), reject()
  - 대기(pending) : 프로미스 객체가 생성되어 대기 중인 상태
  - 이행(fulfilled) : resolve()를 실행시켰을 때의 상태
  - 거부(rejected) : reject()를 실행시켰을 때의 상태
  - 개선된 promise 사용방법 : 함수 내부에 반환 값으로 프로미스를 사용한다.
  - 체이닝 메서드
    - 함수의 리턴을 객체로 리턴
- try catch
  - 에러발생 시 이후에 대한 코드를 무시하는 catch로 처리

- Async Fnc : 항상 promise를 반환 만약 promise를 반환하지 않는다면 암묵적으로 promise 반환
  - await : async 함수 내에서 사용되며 async 함수의 실행을 일시 중지하고 전달된 promise를 기다린 후 async 함수 완료

- XHR(XMLHttpRequest) : AJAX 요청을 생성하는 API

---

## [axios](https://github.com/100SeongJun/JS/blob/main/step07_apply/axios_fetch_lab05.html)

- axios : 비동기 통신을 위해 사용되는 라이브러리(Promise 기반)
|Method|내용|
|:-------:|:-------:|
|axios.get| 정보를 요청|
|axios.post|정보 입력(생성)|
|axios.put|정보수정(전체 정보 수정(덮어쓰기))|
|axios.patch|입력한 정보만 수정|
|axios.delete|정보 삭제|

- fetch : 자바 내장 라이브러리(Promise 기반)
  - axios와 같은 method 존재


### 
