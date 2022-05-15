# Java Script

## [변수&연산자](https://github.com/100SeongJun/JS/blob/main/step02_data/data.md)

## [조건 반복문](https://github.com/100SeongJun/JS/blob/main/step03_control_flow/control.md)

## [함수 & 스코프](https://github.com/100SeongJun/JS/blob/main/step04_function/function.md)

## [객체와 배열](https://github.com/100SeongJun/JS/blob/main/step05_object/object.md)

---

- [HTTP통신방법](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP)

![http요청](https://mdn.mozillademos.org/files/13687/HTTP_Request.png)

![http상태코드](https://developer.mozilla.org/ko/docs/Web/HTTP/Status)
HTTP는 통신을 할 때 사용하는 규칙

- 1.line(!) : 요청방식(Get,Post,Put,Delete ...)
- 2.Header(key:value)) : 기본적인 데이터 (request/ date / host/ content type- [MIME](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/MIME_Types), body 부분의 미디어 타입)

- 3.Body : 데이터 값 (필수로 지정돼있지 않음) 데이터를 전달 받을 수 있는 공간 / 삭제된 내용은 Body에서 확인할 수 없음
  - 실제 데이터(Request - 전송하는 데이터, Response - 반환하는 데이터)
  - 전송 데이터 혹은 반환 데이터가 없다면 - Body는 비어 있을 수 있음

- XHLHTTPResquest(XHR) : 서버와 비동기로 상호작용 하기 위해 사용되는 객체
  - [XML](https://ko.wikipedia.org/wiki/XML) : 마크업 언어(태그(<>)로 구성) / 데이터를 구조화하여 보여주는 언어
