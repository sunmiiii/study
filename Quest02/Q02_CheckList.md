# Checklist  
### 1. CSS를 HTML에 적용하는 세 가지 방법은 무엇일까요?  
1-1 세 가지 방법 각각의 장단점은 무엇일까요?  
|      | 내부 | 인라인 | 외부 |
| ---- | ----- | ---- | ---- |
| 장점  | 인라인보다 재 사용, 변경, 적용 가능 | 직관적인 확인 가능 | 코드 직접적 노출X, 코드 재사용성,유지보수 편리|
| 단점 | 코드 노출(보안취약), 코드 재사용성, 유지보수 불편 | 코드 노출(보안취약), 코드 재사용성, 유지보수 불편, 중복코드시 비대해짐| 지속적인 유지보수, 규모가 클수록 복잡해 질 수 있음 |
| 사용처 | 내부개발(간단한 개발시에) | 단순한 스타일 하나의 태그에 적용할때 사용 | 실제 배포 시 사용(필수)|  
| 사용법 | \<style> h1{color:red;}</style\>|\<p style="color:red;">hi</p\>|\<link rel="stylesheet" href="index_css.css"\>|

※ 외부방식은 css파일에 style태그를 사용하지 않는다.

### 2. CSS 규칙의 우선순위는 어떻게 결정될까요?  
선언방식 우선순위 : 인라인 > 내부 > 외부  
선택자 우선순위 : id > class > 태그 > 전체  
순서 우선순위 : 나중에 선언 > 먼저 선언  
최상위 우선순위 : !important (나중이든 먼저든 가장 최우선)  
==> 연결하는 css 파일의 수를 최소화하고 선택자를 각 css 파일 안에서 의도한 순서대로 정렬  

### 3. CSS의 박스모델은 무엇일까요? 박스가 화면에서 차지하는 크기는 어떻게 결정될까요?  
HTML Element가 웹 페이지에서 차지하는 공간을 정의한 모델  
각 element는 가운데 실제 element의 내용이 담긴 부분(content), element를 감싸는 경계(border),  
border와 content 사이의 영역(padding), border 바깥의 영역(margin)으로 구성된다.  
※ element들은 웹 페이지 전체 너비만큼의 영역을 차지하는 element를 block-level element,  
컨텐츠가 있는 부분의 너비만큼의 영역을 차지하는 element인 inline element로 나뉜다.  

![css_box](https://user-images.githubusercontent.com/103715464/199361735-bb9552b9-d278-4675-89a5-4fda67b824a6.png)

### 4. float 속성은 왜 좋지 않을까요?  
먼저 float이란, 한 요소가 보통 흐름으로부터 빠져나와서 텍스트 및 인라인 요소가 그 주위를 감싸는  
자기 컨테이너의 좌우측을 따라 배치되어야함을 지정한다.  
float을 이용해 레이아웃을 작성할 때, 부모 요소가 자식 요소의 크기를 반영하지 못하는 문제가 발생  
자식요소에 float를 설정하면 부모요소의 높이가 초기화 되어 사라지게 됨
(float속성은 clear 하지않는다면 계속 상속됨)

### 5. Flexbox(Flexible box)와 CSS Grid의 차이와 장단점은 무엇일까요?  

|    | flexbox  | grid |
|----|----------|------|
|장점|요소 컨트롤이 쉬움, 유연한 레이아웃 구현| 간단하게 2차원 레이아웃 관리가능|
|단점|구형 브라우저에서 적용 안됨 | 모든 브라우저에서 지원하지 않음|
|차이|1차원으로 수평, 수직 영역 중 하나의 방향으로만 레이아웃 나눔|2차원으로 수평 수직 동시에 영역 나눔|

### 6. CSS의 비슷한 요소들을 어떤 식으로 정리할 수 있을까요?  
반복적인 디자인 요소를 적용시 원하는 선택자를 선택하여 적용  
|선택자|사용법|
|-----|------|
|전체선택자| * { color:red; }|
|아이디선택자| #sun { color:red; }|
|클래스선택자| .mi { color:red; }|
|타입선택자| p { color:red; }|


