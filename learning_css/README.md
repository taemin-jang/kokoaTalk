# 3.Learning CSS

## Html에 CSS를 입히는 방법 2가지

1. inline css - head 태그 안에 style 태그로 입력한다.
2. external css - style.css 라는 파일을 생성하고 파일 안에 입력한다.

   그리고 head 태그 안에 link 태그로 연결한다.

## CSS 작성 방법

- 가리키는 대상 (Selector)를 쓰고 각 속성을 쓰기 위해 {}열어서 그 안에 속성을 써준다.

  ```css
  h1 {
    color: blue;
    text-decoration: underline;
    font-weight: 800;
    font-size: 20px;
  }

  address {
    text-align: center;
    color: tomato;
  }
  ```

- text-align : center → 텍스트를 중앙정렬

## Cascading

위에서 부터 아래로 차례대로 내려온다.

브라우저가 CSS (Cascading Style Sheet)코드를 읽을 때 cascading 방식, 즉 위에 있는 코드부터 차례대로 읽는다.

## Box (block)

box 옆에는 또 다른 박스가 오지 않는다.

즉 그것을 block이라고 한다.

높이와 너비를 가진다.

- div
- header
- main
- section
- footer
- article
- 등등

## inline

옆에 다른 요소가 올 수 있다.

inline은 높이와 너비를 가질 수 없다.

- 아주 작은 글 (span)
- 링크 (a)
- 그림 (image) 등

- span과 같은 inline에 padding을 적용하면 잘 적용이된다.
- 하지만 margin을 적용하면 좌,우만 적용이 된다
- 그 이유는 inline은 높이와 너비가 없어서 상, 하에 마진을 가질 수 없다.
- 상, 하에 가지고 싶다면 block으로 바꿔야한다.

## display

block → inline or inline → block 변경할 수 있다

### inline-block

box를 inline으로 처리하면 높이와 너비를 가질 수 없다.

근데 inline으로 처리하면서 box까지 하고 싶은 경우 `inline-block`을 쓰면 된다.

하지만 box마다 작은 간격이 있는 점과 반응형 디자인을 지원하지 않다는 점이다.

이 문제를 해결한 것이 `flex`이다

## flex

display : flex 하면 box 형태 그대로 옆으로 간다.

- justify-content - main axis(주축, 기본값=수평) 넓이(width)를 기준으로
  - center → 가운데로 이동
  - flex-end → 맨 오른쪽으로 이동
  - flex-start → 맨 왼쪽으로 이동
  - space-evenly → 자식 엘리먼트 개수 사이에 빈 공간을 같은 크기로 나누어서 배치한다.
  - space-around → 맨 앞 쪽과 맨 뒤쪽 공간은 자식 엘리먼트 사이 공간의 절반과 같다.
  - space-between → 맨 앞 쪽과 맨 뒤쪽 공간을 최소로 줄이고 자식 엘리먼트 사이 공간은 동일하다.
- align-items - cross axis(교차축, 기본값=수직) 높이(height)를 기준으로
  - center → 가운데로 이동
  - flex-end → 맨 아래로 이동
  - flex-start → 맨 위로 이동
  - stretch → 자식 엘리먼트의 높이(height)를 늘려준다.
- flex-direction - 주축을 바꿀 수 있다.
  - column - 주축을 수직으로 바꾼다
  - row - 주축을 수평으로 바꾼다
- flex-wrap - 자식 엘리먼트들을 강제로 한 줄에 배치할 것인지, 여러행으로 나누어 표현할 것인지 결정한다.
  - nowrap → 기본 설정 값, 부모 엘리먼트 영역을 벗어나더라도 자식 엘리먼트들을 한 줄에 배치한다. 넓이가 원래 설정된 값으로 안될 수도 있다.
  - wrap → 부모 엘리먼트 영역을 벗어나면 자식 엘리먼트들을 여러 행으로 나누어 배치한다.
    원래 설정된 넓이 값을 유지한다.
  - wrap-reverse → 주축이 수평이면 방향이 오른쪽에서 왼쪽 방향이고, 주축이 수직이면 아래에서 위쪽 방향으로 바뀐다.

### flexbox의 3가지 규칙

1. 자식 엘리먼트에는 어떤 것도 적지 말아야 한다. 부모 엘리먼트에만 적어야 한다.
   부모 엘리먼트(display : flex)
2.

## box-sizing

### margin

box의 border(경계)의 바깥에 있는 공간이다

- margin값을 1개 줄 경우
  - margin: (상, 하, 좌, 우)
- margin값을 2개 줄 경우
  - margin: (상, 하) (좌, 우)
- margin값을 3개 줄 경우
  - margin: 상 (좌, 우) 하
- margin값을 4개 줄 경우
  - margin: 상 우 하 좌

### padding

box의 border(경계)로부터 안쪽에 있는 공간이다.

### border

box의 경계선이다.

inline과 block에 모두 적용이 된다.

- border: 굵기(2px) 스타일(solid, dotted) 색깔(black)

## id

⇒ #id로 css 적용할 수 있다.

## Class

class는 여러개의 속성들이 공용으로 사용할 수 있는 스타일 형식이고, 중복이 가능하다.

⇒ .class로 css 적용할 수 있다.

### \*는 모든 요소를 뜻한다.

## collapsing margin (마진 상쇄)

한 box의 경계가, 또 다른 box의 경계와 만날 때 일어나고 두 box의 margin은 같아지며 둘 중 큰 margin으로 적용된다. 상, 하에서만 일어나는 현상

1. 인접 형제 박스 간 상하 마진이 겹칠 때

   겹쳐진 두 마진 값을 비교해, 더 큰 마진 값으로 상쇄해 렌더링한다.

   만약 겹쳐진 두 값이 동일할 경우, 중복을 상쇄해 렌더링한다.

   ![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/023f96dc-a6cd-45b1-85c1-eb2713232129/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220904T093543Z&X-Amz-Expires=86400&X-Amz-Signature=071df9e60aaf1673467429300cccd122759e321bc2b85be8aaa1f5c067d05cfe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

2. 빈 요소의 상하 마진이 겹칠 때

   ‘빈 요소’란 높이가 0인 상태의 블록 요소를 말한다.

   - height / min-height / padding / border 등 상하로 늘어나는 프로퍼티 값을 명시적으로 주지 않았거나
   - 내부에 Inline 콘텐츠가 존재하지 않는 요소

   이 경우 위와 아래를 가르는 경계가 없어서 자신의 상단 마진의 값과 하단 마진의 값을 비교해 더 큰 값으로 상쇄한다.

   만약 겹쳐지는 두 값이 동일할 경우, 중복을 상쇄한다.

   ![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7600715b-efe5-46b4-8229-ab944bcebc03/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220904T093551Z&X-Amz-Expires=86400&X-Amz-Signature=603fab46d1657726ff324c5e67fe3c42e64a77923211155861e5abb695fd6f49&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

3. 부모 박스와 첫 번째(마지막) 자식 박스의 상단(하단) 마진이 겹칠 때

   브라우저는 부모 박스와 첫 번째(마지막) 자식 박스 간의 경계를 그 사이에 있는 border / padding / inline 콘텐츠 유무로 판단한다.

### 마진 상쇄 규칙 적용

- 마진 상쇄는 인접한 두 박스가 온전한 block-level 요소일 경우에만 적용된다.
- 마진 값이 0이더라도 상쇄 규칙은 적용된다.
- 좌우 마진은 겹치더라도 상쇄되지 않는다.

### 마진 상쇄 규칙 예외

- 박스가 `position : absolute` 된 상태
- 박스가 `float : left / right` 된 상태 (단, clear 되지 않은 상태)
- 박스가`display : flex` 일 때 내부 flexbox item
- 박스가 `display : grid` 일 때 내부 grid item

## position

위치를 옮기고 싶을 때 사용

### fixed

스크롤해도 항상 제자리에 머무른다.

`초기 위치에 고정되어 있지만(이동을 다 한 뒤에 고정을 시킨다)`, top, left, right, bottom 중 하나만 수정해도 margin과 초기 위치가 무시되고 서로 다른 레이어에 위치하게 되어 원래 위치가 무시된다.

그리고 가장 위에 위치하게 된다.

### static

position의 default값

### relative

top, bottom, left, right 속성을 사용하여 위치 조정을 할 수 있다.

엘리먼트가 `처음 위치한 곳을 기준`으로 수정한다.

### absolute

`가장 가까운 relative 부모를 기준`으로 이동시켜준다

가장 가까운 relative 부모를 못 찾을 경우 body를 기준으로 이동한다.

(꼭 relative일때 뿐 아니라 static을 제외한 다른 포지션을 갖는 경우(fixed, sticky등)도 기준으로 이동한다.

### 기존에 알고 있던 selectors 3가지 방법

1. 태그의 이름 쓰기
2. .클래스 이름 쓰기
3. #id 이름 쓰기

## pseudo selectors

조금 더 세부적으로 엘리먼트를 선택하게 해준다.

- `div:last-child{}` - div들 중 마지막 자식을 선택하게 해준다.
- `div:first-child{}` - div들 중 첫번째 자식을 선택하게 해준다.
- `span:nth-child(even){}` - span 중 짝수개를 선택하게 해준다(괄호에 들어가있는 조건을 기준으로 결정된다)
- `input:required {}` - required인 input 태그를 선택하게 해준다.
- `::placeholder{}` - placeholder의 값만 스타일링 할 수 있다.
- `::selection{}` - 텍스트를 드레그(select)할 때 발생한다.
- `::first-letter` - 첫 글짜에만 적용이된다.
- `::first-line`- 첫 줄에만 적용이된다.

### Combinator

- `부모 자식{}` - 부모 안에 자식을 선택하게 해준다.
- `부모 > 자식{}` - 부모 바로 밑에 자식을 선택하게 해준다.
- `p + span{}` - p의 바로 다음으로 오는 형제인 span을 선택하게 해준다.
- `p ~ span{}` - p의 바로 다음으로 오지 않아도 형제인 span이 있다면 선택하게 해준다.

### Attribute

- `input[type=”password”]{}` - input태그에 type=”password”를 선택하게 해준다.
  `태그[속성 = “속성값”]`
- `태그[속성 ~= “속성값”]{}` - 속성에 속성값이 독단적으로 있으면 선택해준다.
  ex) `input[placeholder~=”name”]{}` - placeholder에 name이라는 단어가 독단적으로 포함되어 있으면 선택 (first name, last name과 같이)
- `태그[속성^=”속성값”]{}` - 속성 값이 속성의 접두사에 속하면 선택해준다.
- `태그[속성$=”속성값”]{}` - 속성 값이 속성의 접미사에 속하면 선택해준다.
- `태그[속성*=”속성값”]{}` - 속성 값이 속성에 한 번 이상 포함이 되면 선택해준다.
  ex `[placeholder *=”pass”]{}` - placeholder=”password” 이므로 pass가 포함되어 있어서 선택이된다.

## State

- `:active` - 마우스로 대상을 클릭했을 때
- `:hover` - 마우스 커서가 대상 위에 있을 때
- `:focus` - 마우스나 키보드로 대상을 선택했을 때
- `:visited` - 링크에만 적용되며, 링크를 방문하고나서 적용이 된다.
- `focus-within` - focused인 자식을 가진 부모 엘리먼트에 적용한다.

## Color

### 컬러 시스템 3가지

1. 16진수 컬러 (hexadecimal color)

   ex) #FFFFFF

2. RGB 방식

   ex) rgb(255, 255, 255) ⇒ rgb(red, green, blue)

3. rgba

   ex) rgba (red, green, blue, alpa(투명도 0~1))

## Variable (custom properties)

variable은 css를 프로그래밍 언어처럼 보여준다.

변수를 선언하고 변수에 값을 집어넣어 준 후 변수를 사용하므로써 작업량을 줄어줄 수 있다.

### :root

:root는 기본적으로 모든 document의 뿌리가 된다. 즉, 출발점이 되는 것.

여기에 변수 이름을 쓰고 값을 저장하고 변수를 사용할 곳에 `var(변수 이름)`을 해주면 된다

### 변수 이름 짓기

- 변수는 dash(-) 2개 하고 변수 이름을 써줘야 한다.
- 빈 공간이 있다면 dash로 채워줘야 한다.
- ex) `--main` , `--main-color` 이런식으로
