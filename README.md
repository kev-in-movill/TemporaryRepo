# CSS Guideline
##### 상기 문서는 CSS Module 및 UI 개발 공통화를 위해 작성하였습니다.

### 1. Preprocessor
- scss 언어로 개발한다.

### 2. Unit
- 컴포넌트 단위로 개발되며 컴포넌트는 자신의 최소 정보를 가지고 있다.
- 컬러, 아웃라인, 폰트, hover, focus, shadow, animate 등으로 구성된다.

### 3. Responsive Design
- 모든 컴포넌트는 반응형 디자인을 고려하여 개발한다.
- 컴포넌트는 자신의 min size 와 max size 정보를 가지고 있어야 한다.
- 가능하면 vh, vmin, vmax, em 등을 활용하여 확장성을 보장한다.
- 표준 spacing 지정하여, 동일한 UI 비율/간격의 통일성을 확보한다.

### 4. Color Spectrum
- 작업에 사용하는 컬러는 정확한 코드를 상수로 활용한다.
- light, dark, primary, secondary 등 컬러의 스펙트럼 지정하고 활용할 수 있도록 한다.
- info, warning, danger, pass, fail 등 메시지별 컬러 스펙트럼을 통일한다.
- 정의된 컬러 스펙트럼은 모든 컴포넌트에 적용 가능해야 한다.

### 5. Naming Rule
- scss 를 글로벌/지역 변수로 작성하여 중복을 줄이고 재활용을 최대화 한다.
- 공통 레이아웃을 먼저 구성하며, 섹션별 예약어를 지정하여 활용한다.
- CSS prefix 는 서비스명으로 통일한다.
- (React 컴포넌트도 prefix 를 서비스명으로 쓰기 때문.. 둘을 다루기에 명확해 짐)

### 6. Usage 
- 각 컴포넌트는 활용 가능한 자신의 최소 정보를 가진다.
- 각 컴포넌트의 default 값으로 Full Width, No margin, No padding
- 컴포넌트의 지정 값(size, padding 등) Wrapper에서 상속받아 정의한다.
- 이렇게 정의된 컴포넌트를 배치/그룹화 하는 Wrapper 재정의하고 상속하여 구성
- 그룹 Wrapper 조합이 레이아웃의 구성이 된다 ex. Header, Content, Footer
- UI와 Wrapper 들은 자신의 최소데이터만 가지고 있고, 구성은 상위 Wrapper 에서 상속받아 화면을 구성.

### 7 Layout 구성과 React 컴포넌트 개발 예시
<img width="1024px" src="https://user-images.githubusercontent.com/51313376/61119815-98801c00-a4d6-11e9-84d4-d65c5162b1ec.jpeg" />

<img width="1024px" src="https://user-images.githubusercontent.com/51313376/61119977-eac13d00-a4d6-11e9-86f6-de1fb47737e9.jpeg" />

<img width="1024px" src="https://user-images.githubusercontent.com/51313376/61120030-0298c100-a4d7-11e9-803b-b6004b6157ce.jpeg" />

### 8. Porting 
- scss 데이터는 Styled Component 를 활용하여 React 네이티브 컴포넌트로 포팅.
- Stateless Component 로 개발하고, 상태를 관리하는 Container 에서 Composition.
- 부모 상속 정의가 필요한 이유는 리액트 컴포넌트로 재활용을 하기 위함.
 

