## 1. React 시작하기

- create-react-app 으로 리액트 프로젝트 생성 npm init react-app <폴더이름> 혹은 폴더를 VS Code로 열고 터미널에서 npm init react-app .

- 개발 모드 실행 : npm run start
- 개발 모드 종료 : Ctrl + C

- 리액트 개발자 도구 설치 : chrome 웹스토어에서 React Developer Tools 확장프로그램 설치
- 확장프로그램 설치시 개발자 도구에 components, profiler 탭 새로 생성됨. 리액트 페이지에서만 사용가능.

## 2. 주사위 게임 프로젝트 세팅

- public에서는 index.html 파일만 남기고 다 지우기, index.html 파일에서 사용하지 않을 코드 정리
- src에서는 index.js 파일만 남기도 다 지우기, index.js 파일에서 사용하지 않을 코드 정리

## 3. 인덱스 파일에서 하는일

- react가 실행되면 index.html이 가장 먼저 실행되고 그다음 index.js가 실행된다.
- index.js에서는 ReactDOM.render메소드로 첫번째 argument를 활용해서 html 요소를 만들고, 두번째 argument 값에 그 요소를 넣어준다.
- index.js에서 root id는 index.html에서 body태그에 있는 root를 말한다.
- ReactDOM.render메소드는 index.js에서 보통 한번 실행된다.

## 4. JSX

- JSX 문법은 자바스크립트와 html을 섞어 쓰는 자바스크립트 확장된 버전이다.
- JSX에서 자바스크립트 확장 문법이기 때문에, html문법을 완전하게 사용하고 있지 않다.
- 자바스크립트에서는 객체지향 키워드로 Class를 사용하기 때문에 css문법으로 class가 아닌 className을 사용해야 한다.
- html에서 for라는 속성은 label 태그에서 input 태그와 함께 사용되는 속성이고, 자바스크립트에서 for는 반복문으로 사용된다.
- 따라서 JSX 문법에서 for라는 html 속성을 사용하려면 htmlFor로 작성해야한다.
- 이벤트 핸들러의 경우(ex : onblur="", onfocus="", onmousedown="")도 html에서는 소문자로 작성되지만 JSX에서는 두번째 단어를 대문자로 작성해야한다.(onMouseDown, onFocus, onBlur - 카멜케이스)

## 5. 프래그먼트

- JSX에서는 여러개의 태그들을 하나의 태그(div)로 감싸줘야한다.
- 감싸주는 태그(div)를 만들고 싶지 않을 경우 Fragment 태그로 감싸주면 자동으로 import되어 사용가능하다.

```
<Fragment>
    <p>안녕</p>
    <p>리액트!</p>
</Fragment>
```

- Fragment 태그는 <> 이름없는 태그 축약형 형태로 많이 사용한다.

```
<>
    <p>안녕</p>
    <p>리액트!</p>
</>
```

## 6. JSX에서 자바스크립트 사용하기

- JSX 문법에서 중괄호를 사용하면 자바스크립트 표현식을 사용할 수 있다.
- 자바스크립트 표현식만 가능하기 때문에, if문, for문, 이벤트함수 등과 같은 문장은 사용할 수 없다.
- 변수입력 뿐 아니라 요소의 속성값 입력 및 함수 사용(JSX에서는 addEventlistenr가 아닌 요소의 속성값 형태)을 위해 {}를 이용한 자바스크립트 표현식을 사용할 수 있다.
