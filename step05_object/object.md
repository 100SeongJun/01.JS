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

- 조회 : 배열명[index]; >>
- 길이 : 배열명.length
| 이름 | : 명령어 : | : 설명 :|
|------|:-----------------------------: | :-------- |
|조회|배열명[index]|배열의index번호를 조회|
|길이|배열명.length|배열의 크기 출력|