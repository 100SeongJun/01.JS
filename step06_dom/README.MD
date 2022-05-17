# 문서객체모델

## [DOM](https://github.com/100SeongJun/JS/blob/main/step06_dom/dom_lab01.html)

- Document Object Model
- 페이지의 모든 컨텐츠를 객체로 표현하는 모델
- DOM을 계층적으로 표현, 계층적인 단위 Node (노드, 관계성 개념)
- Document 객체 : 웹페이지 자체, 따라서 모든 HTML요소에 접근하기 위해서는 Document 객체로 부터 시작
- DOM Selection (선택)

|명령어|코드|설명|
|getElementBy##|document.getElementsByClassName('btn');|Id값을 통해 객체 접근|
|querySelector| document.querySelector('.btn');|css선택자를 사용하여 요소 찾기 / 최상단 요소만 로직에 포함|
|querySelectorALL|document.querySelectorAll('.btn');|nodelist 반환|
|childNodes[i]|console.log(document.childNodes[1].childNodes[2]);|노드를 통해 접근|
|createElement|document.createElement('hr');|hr태그 생성|

## [이벤트](https://github.com/100SeongJun/JS/blob/main/step06_dom/event_lab02.html)

- 인라인 방식

```javascript
        function clickFunc(){
            describeElement.innerText='계좌조회서비스';
        }
```

- 프로퍼티 방식
  - 하나에 대한 함수만 지정가능(여러 개의 이벤트 적용시 한계점을 가짐)

```javascript
  check.onclick =function clickFunc(){
  describeElement.innerText=('계좌조회서비스');
  };
```

- 이벤트 핸들러

```javascript
  checkElement.addEventListener('click', 
   function clickFunc()
   {
  describeElement.innerText='계좌조회서비스';
   });
```

- 이벤트 종류
  - 마우스 이벤트 (Onclick ,mouseup,mousedown,mousemove,mouseover)
  - 키보드 이벤트

## [이벤트실습](https://github.com/100SeongJun/JS/blob/main/step06_dom/event_apply_lab03.html)

1. 이벤트 흐름: 이벤트가 발생하는 html 요소는 계층구조로 돼있어서 우리가 알게 모르게 주변 요소에 영향을 미침
2. 이벤트 전파(Propagation) : 전파되는 방향을 기준으로 버블링,캡처링 발생

- 버블링 : 자식요소가 부모요소에게 영향을 미침
- 캡처링 : 부모요소에 있는 이벤트가 자식요소에게 전달됨
- 형제요소는 서로 영향을 미치지 않음
