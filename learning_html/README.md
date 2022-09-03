# 2.Learning HTML

## HTML Tag

- ‘여기부터 여기까지가 제목이야’ 라고 말해주는 것이 HTML Tag라고 한다.
- <h1> text </h1> 이 두 태그 사이에 넣는 내용이 무언가가 된다.
- <h1> 태그를 열어 준 것이고, </h1> /가 있으면 태그를 닫아준 것이다.
- 아무 의미가 없는 태그를 적어도 되지만 브라우저에서 원하는 대로 작동은 안된다.

### h1(header number 1)

제목

### ul(unordered list)

순서가 없는 리스트

### ol(ordered list)

순서가 있는 리스트

### a(anchor)

다른 링크로 이동하게 해줌

a 태그에는 다른 부가적인 정보(attribute)가 필요하다

- href (HTTP reference || hyperlink reference) - 이동할 곳을 알려주는 속성
- target - 기본값은 \_self ⇒ 현재 페이지에서 이동할 페이지를 띄워줌
  \_blank ⇒ 새로운 페이지를 열어서 이동할 페이지를 띄워줌

### img

이미지를 넣기 위한 태그

img 태그는 self-closing tag(자체 닫기 태그)이다

- src (source) - img안에 사진을 집어 넣음(이미지 주소나, 파일 경로를 입력해줘야함)

### path notition(경로 표기법)

⇒ img/logo,jpg

## HTML 문서 규칙

`<!DOCTYPE html>` → 브라우저에게 이건 text 파일이 아니라 html 문서라고 알려주는 코드

`<html>` → html 태그 사이에 넣는게 html 코드가 된다.

`lang` → 구글, 네이버, bing 같은 검색엔진에게 우리 사이트가 사용되는 언어가 무엇인지 알려준다.

`<head>` → head 태그는 웹사이트의 외부적으로 보이지 않는 환경을 설정한다.

`<title>` → 페이지의 제목을 설정해주는 태그

`<meta>` → 부가적인 정보를 제공해주는 태그 (content, name attribute를 가짐)

`name` → description 을 사용하면 검색했을때 우리 사이트의 대한 설명 부분을 보여준다. 내용은 content에서 작성한 것으로 보여짐.

`content` → 설명 내용을 적어주는 곳.

`<meta charset="utf-8"/>` → 브라우저에게 text를 어떻게 그려달라는지 말해주는 부분

`<meta property="og : 입력">` → og(open graph) : ~~ 로 하는 것은 카카오톡으로 링크 공유했을 때 최적화된 데이터로 가지고 갈 수 있도록 설정하는 것 (og : ~~ 네이버 , 카카오톡 / fb : ~~ 페이스북 / twitter : ~~ 트위터 등등등)

`og : title` → 공유됐을 때 보여지는 제목

`og : description` → 공유됐을 때 보여지는 설명내용

`og : image` → 공유됐을 때 보여지는 이미지

`<link>`

`rel` → relationship의 줄임말로 shortcut icon 을 입력해주면 title의 아이콘을 가리킨다.

`sizes` → 아이콘 사이즈 결정

`href` → 아이콘 경로 설정

`<body>` → body 태그는 사용자가 볼 수 있는 content를 보여준다.

## form 태그 속성

`type` → input의 유형을 결정해준다.

- color : 색을 선택할 수 있다.
- password : 입력하면 \*\*\*로 출력된다.
- text : type의 기본값으로 입력하면 입력한대로 출력된다.
- submit : 버튼 역할을 하며, 누르면 form 정보를 전송한다(새로고침이 됨).

`placeholder` → input 값에 무엇을 입력해야하 하는지에 대한 정보를 제공한다.

- name이라고 입력해놓으면 input 창에 이름을 입력해야하는 부분이라고 알려준다.

`value` → 내용을 바꿔준다.

- type = “submit” 이면 submit 이란 이름으로 버튼이 생기는데 value 값을 지정해주면 value 에 입력된 값으로 이름이 바뀐다.

`disable` → input의 기능을 하지 못하게 한다.

`required` → input의 검증을 할 수 있다. required가 들어간 input 은 무조건 작성해야한다.
`minlength` → input 길이의 최소 값을 설정해 준다.

## label 태그

label은 input과 함께 사용해야한다.

`for` → input의 `id` 와 동일한 값이여야 한다.

## id - 태그는 하나의 값만 가질 수 있다, id 값은 고유해야한다.

## 시멘틱태그(semantic tag)

문서를 보기만 해도 그 의미를 짐작할 수 있는 태그\

되도록 시멘틱 태그를 쓰도록 하자

- header 태그
- main 태그
- footer 태그
- 등등

## non-semantic tag

- div
- span
- 등등

## 총 정리한 코드

[https://codepen.io/taemin-jang/pen/eYrYWBr](https://codepen.io/taemin-jang/pen/eYrYWBr)
