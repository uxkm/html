# 10.1. HTML4에서의 문서 구조

 문서의 구조, 즉 `<body>`와 `</body>` 사이에 있는 것의 의미론적 구조는, 페이지 내용을 사용자에게 전달하는 데 중요한 토대가 됩니다.  
HTML4에선 일종의 섹션과 그 하위 섹션으로 구분하는 개념을 써서 문서의 구조를 표현합니다.  
섹션은 HTML `<div>`요소와 함께 그 안에 있는 제목을 정의하는 HTML 제목 요소\(`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, 혹은 `<h6>`\)를 써서 정의됩니다.  
이런 HTML 구획 요소와 HTML 제목 요소의 관계가 문서의 구조와 그 아웃라인을 결정짓게 됩니다.

## HTML4 기본 레이아웃

```text

<div class="wrap">
	<div class="header">
		상단 영역
	</div>
	<div class="main">
		<div class="sidebar">
			왼쪽 그룹(왼쪽 메뉴)
		</div>
		<div class="csection">
			콘텐츠 영역
		</div>
	</div>
	<div class="footer">
		하단 영역
	</div>
</div>
```

## HTML4 콘텐츠 기본 구조

```text

<div class="section" id="html-element">
	<h1>HTML</h1>
	<p>이번 섹션에선, HTML 기본 구조에 대해 알아보겠습니다.
	...섹션 내용 진행 중...
	<div class="subsection" id="forest-habitat">
		<h2>HTML 이란?</h2>
		<p>HTML은 Tim Berners-Lee, Robert Cailliau 및 1989 년 부터 시작된 사람들에 의해 처음 만들어졌습니다.
		...하위 섹션 내용 진행 중...
	</div>
</div>

<!--
위의 구조는 다음과 같은 문서 아웃라인을 가지게 됩니다.
1. HTML
	 1.1 HTML 이란?


위와 같이 새로운 섹션을 정의할 때 <div> 요소가 꼭 필요한 것은 아닙니다. 단순히 HTML 제목 요소만 있으면 새로운 섹션이 시작됨을 자동으로 암시해 줍니다.
<h1>HTML</h1>
<p>이번 섹션에선, HTML 기본 구조에 대해 알아보겠습니다.
...섹션 내용 진행 중...
<h2>HTML 이란?</h2>
<p>HTML은 Tim Berners-Lee, Robert Cailliau 및 1989 년 부터 시작된 사람들에 의해 처음 만들어졌습니다.
...하위 섹션 내용 진행 중...
<h2>HTML 기본구조</h2>
<h1>CSS</h1>

위의 구조는 다음과 같은 문서 아웃라인을 가지게 됩니다.
1. HTML
   1.1 HTML 이란?
   1.2 HTML 기본구조
2. CSS
-->
```

