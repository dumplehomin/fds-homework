#css 선택자
- 일반 선택자
- 속성 선택자
- 가상 클래스
- 가상 요소

---
###일반 선택자

유형 | 설명 | Safari 5| Chrome 8 | FireFox 3.6 | Opera 11 | IE9 | IE8 | IE7 | IE6
--- | - | - | --- | --- | --- | --- | --- | --- | ---
* | 모든 요소 선택 | O | O | O | O | O | O | O | O
#id | id로 지정된 요소 선택 | O | O | O | O | O | O | O | O
.class | class로 지정된 요소 선택 | O | O | O | O | O | O | O | O
E | E 요소를 선택 | O | O | O | O | O | O | O | O
E>F | E 요소의 자식인 F 요소 선택 | O | O | O | O | O | O | O | X
E+F | E 요소를 뒤의 F 요소 선택 | O | O | O | O | O | O | O | X
E~F | E 요소가 앞에 존재하면 F를 선택 | O | O | O | O | O | O | O | X
---
###속성 선택자

유형 | 설명 | Safari 5| Chrome 8 | FireFox 3.6 | Opera 11 | IE9 | IE8 | IE7 | IE6
--- | --- | --- | --- | --- | --- | --- | --- | --- | ---
E[foo] | ‘foo’ 속성이 포함된 E를 선택 | O | O | O | O | O | O | O | X
E[foo="bar"] | ‘foo’ 속성의 값이 ’bar’와 일치하는 E를 선택 | O | O | O | O | O | O | O | X
E[foo~="bar"] | ‘foo’ 속성의 값에 ’bar’가 포함되는 E를 선택 | O | O | O | O | O | O | O | X
E[foo|="en"] | ‘foo’ 속성의 값이 ’en’ 또는 ’en-’ 으로 시작되는  E를 선택 | O | O | O | O | O | O | O | X
E[foo^="bar"] | ‘foo’ 속성의 값이 ’bar’로 정확하게 시작하는 요소 선택 | O | O | O | O | O | O | O | X
E[foo$="bar"] | ‘foo’ 속성의 값이 ’bar’로 정확하게 끝나는 요소 선택 | O | O | O | O | O | O | O | X
E[foo*="bar"] | ‘foo’ 속성의 값에 ’bar’를 포함하는 요소 선택 | O | O | O | O | O | O | O | X
---

###가상 클래스

유형 | 설명 | Safari 5| Chrome 8 | FireFox 3.6 | Opera 11 | IE9 | IE8 | IE7 | IE6
--- | --- | --- | --- | --- | --- | --- | --- | --- | ---
E:link | 방문하지 않은 E를 선택 | O | O | O | O | O | O | O | O
E:visited | 방문한 E를 선택 | O | O | O | O | O | O | O | O
E:hover | 마우스가 올라가 있는 동안 E를 선택 | O | O | O | O | O | O | O | O
E:active | 마우스 클릭 또는 키보드(enter)가 눌린 동안 E를 선택 | O | O | O | O | O | O | O | X
E:focus | focus가 머물러 있는 동안 E를 선택 | O | O | O | O | O | O | X | X
E:first-child | 첫 번째 자식 요소가 E라면 선택 | O | O | O | O | O | O | O | X
E:last-child | E 요소 중 마지막 자식이라면 E 선택 | O | O | O | O | O | X | X | X
E:nth-child(n) | 그 부모의 n번째 자식이 앞으로부터 지정된 순서와 일치하는 E 라면 선택 | O | O | O | O | O | X| X | X
E:nth-last-child(n) | n번째 자식이 뒤로부터 지정된 순서와 일치하는 요소가 E 라면 선택 | O | O | O | O | O | X | X | X
E:nth-of-type(n) | E 요소 중 앞으로부터 순서가 일치하는 n번째 E 요소 선택 | O | O | O | O | O | X | X | X
E:nth-last-of-type(n) | E 요소 중 끝으로부터 순서가 일치하는 n번째 E 요소 선택 | O | O | O | O | O | X | X | X
E:first-of-type | E 요소 중 첫번째 E 선택 | O | O | O | O | O | X | X | X
E:last-of-type | E 요소 중 마지막 E 선택 | O | O | O | O | O | X | X | X
E:only-child | E 요소가 유일한 자식이면 선택 | O | O | O | O | O | X | X | X
E:only-of-type | E 요소가 같은 타입이면 선택 | O | O | O | O | O | X | X | X
E:first-line | E 요소의 첫 번째 라인 선택 | O | O | O | O | O | O | O | X
E:first-letter | E 요소의 첫 번째 문자 선택 | O | O | O | O | O | O | O | X
E:not(s) | s가 아닌 E 요소 선택 | O | O | O | O | O | X | X | X
---

###가상 요소

유형 | 설명 | Safari 5| Chrome 8 | FireFox 3.6 | Opera 11 | IE9 | IE8 | IE7 | IE6
--- | --- | --- | --- | --- | --- | --- | --- | --- | ---
E::lang(fr) | HTML lang 속성의 값이 ’fr’로 지정된 E를 선택 | O | O | O | O | O | O | X | X
E::before | E 요소 전에 생성된 요소 선택 | O | O | O | O | O | O | X | X
E::after | E 요소 후에 생성된 요소 선택 | O | O | O | O | O | O | X | X
E::root | 문서의 최상위 루트 요소 선택 | O | O | O | O | O | X | X | X
E::empty | 텍스트 및 공백을 포함하여 빈 자식을 가진 E를 선택 | O | O | O | O | O | X | X | X
E::target | E의 URI의 대상이 되면 선택 | O | O | O | O | O | X | X | X
E::enabled | 활성화된 폼 컨트롤 E요소 선택 | O | O | O | O | O | X | X | X 
E::disabled | 비활성화된 폼 컨트롤 E요소 선택 | O | O | O | O | O | X | X | X
E::checked | 선택된 폼 컨트롤(라디오버튼,체크박스)을 선택 | O | O | O | O | O | X | X | X
