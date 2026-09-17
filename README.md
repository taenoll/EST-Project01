# EST-Project01

# AVENUE 9

> **Everyday scent, made for the city.**

도시의 하루에서 영감을 받은 가상의 프래그런스 라이프스타일 브랜드 웹사이트입니다.

바쁜 아침의 에스프레소, 퇴근 후 거리의 불빛처럼  
각자의 방식으로 도시를 살아가는 순간을 향으로 기록한다는 콘셉트로 제작했습니다.

---

## 프로젝트 소개

- **프로젝트명**: AVENUE 9
- **프로젝트 유형**: HTML / CSS 반응형 웹사이트
- **진행 형태**: 팀 프로젝트
- **주요 목표**
  - 시맨틱 HTML 구조 설계
  - Desktop / Mobile 반응형 레이아웃 구현
  - 웹 접근성을 고려한 마크업 및 스타일링
  - CSS Variables를 활용한 디자인 시스템 구축
  - Git / GitHub를 활용한 협업

---

## 페이지 구성

### HOME

- Hero
- About AVENUE 9
- Scent Collection
  - MONDAY 9AM
  - NEW YORK FRIDAYS
- City Editorial
- Products
- CTA
- Footer

### Product Detail

- MONDAY 9AM
- NEW YORK FRIDAYS
- 제품 이미지
- 향의 주요 노트
- 제품 상세 정보
- Ingredients

### Products

- AVENUE 9의 제품 목록

---

## 사용 기술

- HTML5
- CSS3
- Git
- GitHub
- Figma

---

## 디자인 시스템

프로젝트 내에서 반복되는 디자인 값을 CSS Custom Properties로 관리했습니다.

```css
:root {
  /* Color */
  --color-bg-page: #f1efeb;
  --color-brand-espresso: #160a03;

  /* Spacing */
  --spacing-md: 16px;
  --spacing-xl: 32px;

  /* Typography */
  --font-family-display: 'Cinzel', serif;
  --font-family-body: 'Inter', sans-serif;
}
```

Color, Spacing, Typography, Font Weight, Border Radius 등의 값을 변수로 관리하여
페이지마다 일관된 디자인을 유지할 수 있도록 구성했습니다.

## 반응형 웹

Desktop과 Mobile 환경에 맞춰 레이아웃이 자연스럽게 변경되도록 구현했습니다.

Grid와 Flexbox를 활용한 레이아웃
Desktop의 다열 구조를 Mobile에서는 1열 구조로 변경
화면 크기에 맞춰 이미지와 텍스트 배치 변경
모바일에서도 메뉴의 터치 영역 확보
콘텐츠가 화면 밖으로 넘치지 않도록 반응형 레이아웃 조정

## 웹 접근성

웹 접근성을 고려하여 다음과 같은 요소를 적용했습니다.

header, nav, main, section, article, footer 등 시맨틱 태그 사용
h1 → h2 → h3의 자연스러운 제목 구조
의미가 있는 이미지에 alt 제공
장식용 이미지에 alt="" 적용
aria-label, aria-labelledby 활용
본문 바로가기 Skip Link 제공
:focus-visible을 이용한 키보드 포커스 표시
상품 카드 hover 효과를 :focus-within에서도 확인 가능하도록 구현
prefers-reduced-motion을 통한 모션 감소 설정 대응

## 주요 구현 내용

1. Scent Collection

Desktop에서는 향수 정보와 이미지 콜라주를 2열 구조로 구성하고,
Mobile에서는 텍스트와 이미지를 위에서 아래로 읽을 수 있도록 1열 구조로 변경했습니다.

전체적인 레이아웃에는 Grid를 사용하고,
이미지가 서로 겹쳐 있는 콜라주 영역에서만 position: absolute를 사용했습니다.

2. Product Card

상품 카드에 마우스를 올렸을 때 이미지가 변경되도록 구현했습니다.

키보드 사용자도 동일한 변화를 확인할 수 있도록
:hover뿐만 아니라 :focus-within 상태도 함께 적용했습니다.

3. Skip Link

키보드 사용자가 반복되는 Header 메뉴를 거치지 않고
본문으로 바로 이동할 수 있도록 Skip Link를 추가했습니다.

```
<a href="#main-content" class="skip-link">본문 바로가기</a>

<main id="main-content" tabindex="-1">
```

4. Responsive Layout

Desktop 디자인을 단순히 축소하는 방식이 아니라
Mobile 환경에서는 콘텐츠 순서와 레이아웃을 다시 배치하여
작은 화면에서도 자연스럽게 읽을 수 있도록 구현했습니다.
