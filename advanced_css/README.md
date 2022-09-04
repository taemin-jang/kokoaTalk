# 4.Advanced CSS

## Transitions

어떤 상태에서 다른 상태로의 “변화”를 애니메이션으로 만드는 방법

- transition은 state(hover, active …)가 없는 요소에 붙어야한다.
- transition: background-color 10s ease-in-out
  ⇒ background-color를 사라졌다가 나타나게 10초 동안 애니메이션을 준 것이다.

## Timing function

- linear - 속도가 일정하다.
- ease - 천천 - 빠름 - 천천
- ease-in - 천천 - 보통
- ease-out - 보통 - 천천
- ease-in-out - 천천 - 보통 - 천천
- cubic-bezier - 커스텀
- steps - 뚝뚝 끊어 보여준다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/466b3b1f-d997-4b55-86c1-db1ee13a8cde/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220904T130659Z&X-Amz-Expires=86400&X-Amz-Signature=d97b94e15b53ccecfdd508bd113e2e3eaf7d085c19c26f7564853dbdda9cbb36&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## 참고

[CSS / 애니메이션 / transition / 속성을 서서히 변화시키는 속성](https://www.codingfactory.net/10953)

## Transformations

한 요소를 변형 시킬 수 있다.

- transformation은 box element를 변형시키지 않는다.
- 옆에 있는 다른 형제(sibling)들에게 영향을 끼치지 않는다.
- margin, padding이 적용되지 않는다. 일종의 3D transformation이기 때문이다.
- margin, padding을 주기 위해 translateX, translateY를 사용하는 것이 아니다.
- 다른 요소의 box를 변형시키지 않고 원하는 요소만 이동시키기 위해서 사용하는 것이다.

## Animation

### 사용법

```css
@keyframes 애니메이션 이름 {
  from {
    /* 여기서 시작 */
  }
  to {
    /* 끝 */
  }
}

@keyframes 애니메이션 이름 {
  0% {
  }

  50% {
  }

  100% {
  }
}

img {
  animation: 애니메이션이름 실행시간 Timing-function 애니메이션-시작지점
    반복횟수 direction fill-mode 재생상태 타임라인(스크롤);
}
```

## Media Queries (반응형)

오직 css만을 이용해서 웹 사이트를 보고 있는 사용자의 스크린의 사이즈를 알 수 있는 방법

### 사용법

```css
@media screen and (max-width: 400px) {
  div {
    background-color: red;
  }
}
```

위 코드가 의미하는 것은, 이 스크린이 400px보다 작으면 div 태그의 배경 색을 빨간색으로 바꾼다.

### Media Queries 주요기능

- `orientation: landscape` - 가로 모드
  `orientation: portrait` - 세로 모드
- `min-width`, `max-width` - 컴퓨터, 휴대폰 둘 다 작동 한다.
- `min-device-width`, `max-device-width` - 휴대폰에서만 작동 한다.
- `aspect-ration` - 레티나디스플레이 감지가능
- `display-mode`
- `inverted-colors`
- `lightlevel`
- `prefers-contrast`
- `resolution`
- `monochrome`

### Media type

- `@media screen{}` - 사용자의 스크린
- `@media print{}` - ctrl + p 누르면 나오는 프린트 화면
