# AVENUE 9

> Everyday scent, made for the city.

도시의 하루에서 영감을 받은 가상의 프래그런스 라이프스타일 브랜드 웹사이트입니다.

바쁜 아침의 에스프레소, 퇴근 후 거리의 불빛처럼  
도시에서 보내는 여러 순간을 향으로 표현했습니다.

---

## 프로젝트 소개

- 프로젝트명: AVENUE 9
- 프로젝트 유형: HTML / CSS 반응형 웹사이트
- 진행 방식: 팀 프로젝트

### 프로젝트 목표

- 시맨틱 HTML을 활용한 웹 구조 작성
- Desktop / Mobile 반응형 레이아웃 구현
- 웹 접근성을 고려한 마크업
- CSS Variables를 활용한 디자인 시스템 구성
- Git / GitHub를 활용한 협업

---

## 페이지 구성

### HOME

- Hero
- About
- Scent Collection
- City Editorial
- Products
- CTA
- Footer

### Perfume Detail

- MONDAY 9AM
- NEW YORK FRIDAYS
- 제품 이미지
- Main Note
- Details
- Ingredients
- Description

---

## 사용 기술

- HTML5
- CSS3
- Git
- GitHub
- Figma

---

## 주요 구현

### 반응형 레이아웃

Desktop과 Mobile 환경에서 콘텐츠가 자연스럽게 보이도록 레이아웃을 조정했습니다.

- Flexbox와 Grid를 활용한 레이아웃 구성
- Desktop의 다열 구조를 Mobile에서 1열 구조로 변경
- 화면 크기에 따라 이미지와 텍스트 배치 변경
- 모바일 메뉴의 클릭 영역 확보

### 디자인 시스템

반복되는 색상, 간격, 글자 크기 등을 CSS Custom Properties로 관리했습니다.

```css
:root {
  --color-bg-page: #f1efeb;
  --color-brand-espresso: #160a03;

  --spacing-md: 16px;
  --spacing-xl: 32px;

  --font-family-display: 'Cinzel', serif;
  --font-family-body: 'Inter', sans-serif;
}
```

## 웹 접근성

HOME 페이지에서는 다음과 같은 접근성을 고려했습니다.

header, nav, main, section, article, footer 등 시맨틱 태그 사용
자연스러운 제목 구조 구성
의미가 있는 이미지에 alt 제공
장식용 이미지에 alt="" 적용
aria-label, aria-labelledby 사용
본문 바로가기 Skip Link 제공
:focus-visible을 이용한 키보드 포커스 표시
:focus-within을 이용한 상품 카드 키보드 접근
prefers-reduced-motion 대응
CSS 파일 구성
variables.css
색상, 간격, 폰트 크기 등 공통 디자인 값 관리
component.css
Header, Button, Link, Footer 등 공통 컴포넌트 스타일 관리
home.css
HOME 페이지 스타일
perfume.css
향수 상세 페이지 공통 스타일
perfume1.css
MONDAY 9AM 페이지 스타일
perfume2.css
NEW YORK FRIDAYS 페이지 스타일
Troubleshooting

---

### 1. 이미지 배치로 인한 가로 스크롤

HOME의 About 이미지 위치를 맞추기 위해 음수 margin을 사용했을 때
이미지가 viewport 밖으로 넘어가 가로 스크롤이 발생했습니다.

음수 margin 값을 조정하여 디자인을 유지하면서
가로 스크롤이 발생하지 않도록 수정했습니다.

### 2. Absolute 요소의 기준점 문제

향수 상세 페이지의 제품 카드에 position: absolute를 적용했지만
부모 요소에 위치 기준이 없어 원하는 위치에 배치되지 않는 문제가 있었습니다.

부모 요소에 position: relative를 적용하여
해당 영역을 기준으로 위치가 계산되도록 수정했습니다.

### 3. Ingredients 중앙 정렬

Ingredients 영역에서 좌우 이미지의 크기가 달라
Flexbox의 space-between만 사용했을 때 가운데 텍스트가 정확한 중앙에 위치하지 않았습니다.

이미지 / 텍스트 / 이미지 구조를 Grid의 3열 구조로 변경하여
가운데 콘텐츠가 중앙에 배치되도록 수정했습니다.

### 4. Merge Conflict

여러 사람이 공통 CSS 파일을 수정하면서 Merge Conflict가 발생했습니다.

충돌 영역을 직접 확인한 뒤
필요한 코드를 각각 유지하는 방식으로 해결했습니다.

---

## 협업 방식

- 작업별 Branch 사용
- 작업 단위 Commit
- Pull Request를 통한 병합
- 공통 CSS 파일은 팀원 간 확인 후 수정
- Merge Conflict 발생 시 충돌 내용을 확인한 뒤 해결

---

## 폴더 구조

EST-Project01/
├── assets/
│ └── images/
│
├── styles/
│ ├── reset.css
│ ├── variables.css
│ ├── component.css
│ ├── home.css
│ ├── perfume.css
│ ├── perfume1.css
│ └── perfume2.css
│
├── index.html
├── perfume1.html
├── perfume2.html
├── products.html
└── README.md

---

배포

배포 후 링크를 추가할 예정입니다.
