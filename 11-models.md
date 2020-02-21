# 11. 콘텐츠 모델

![&#xC790;&#xB8CC; &#xCD9C;&#xCC98; : https://www.w3.org/TR/html52/dom.html\#content-models](.gitbook/assets/content-venn.png)



> HTML5의 요소는 0개 이상의 카테고리에 속하며, 각 카테고리는 서로 특성이 비슷한 요소끼리 묶어둔 분류이다.
>
> 위 이미지에서 보이는 것처럼, HTML5는 다음과 같은 카테고리들을 사용한다.
>
> 또한, 특정요소는 폼관련 요소로 따로 분류하여 다양한 폼 관련 처리 모델에서 세부적으로 분류한다.
>
> 몇몇 요소들은 특정 요소만의 독특한 요구사항을 가지고 있으며, 어느 카테고리에도 속하지 않는다.

## 컨텐츠 모델 상세설명

### 플로우 콘텐츠 \(Flow Content\)

문서및 어플리케이션의 Body에서 사용되는 대부분의 요소는 플로우 콘텐츠로 분류 된다.

a, abbr, address, area \(map 요소의 자식 요소인 경우\), article, aside, audio, b, bdi, bdo, blockquote, br, button, canvas, cite, code, command, datalist, del, details, dfn, div, dl, em, embed, fieldset, figure, footer, form, h1, h2, h3, h4, h5, h6, header, hgroup, hr, i, iframe, img, input, ins, kbd, keygen, label, map, mark, math, menu, meter, nav, noscript, object, ol, output, p, pre, progress, q, ruby, s, samp, script, section, select, small, span, strong, style \(scoped 속성이 있으면\), sub, sup, svg, table, textarea, time, ul, var, video, wbr, text

1. 일반적으로 아무 플로우 콘텐츠 모델을 포함할 수 있는 콘텐츠 모델은 최소한 하나의 공백이 아닌 텍스트 노드를 포함하거나, 또는 최소한 하나의 임베디드 콘텐츠\(아래 다시 설명\)를 포함하여야 한다. 이러한 결과로 del요소 및 그 자식 요소들은 del요소의 부모 엘리먼트가 될 수 없다.
2. 위의 요구사항은 강력하게 지켜야 할 내용은 아니며, 스크립트로 데이터를 채우기 위해 자리를 잡아 두는 목적 등의 정당한 이유로 요소가 비어 있을 수 있다.

### 메타데이터 콘텐츠 \(Metadata Content\)

웹 문서와 관련된 정보를 표현하는 콘텐츠와 다른 문서와의 관계를 유지하는 콘텐츠입니다.  
메타 데이터 콘텐츠 는 나머지 콘텐츠의 프리젠 테이션 또는 동작을 설정, 다른 문서와 문서의 관계를 설정하거나 다른 "대역 외"정보를 전달하는 콘텐츠입니다.

base, link, meta, noscript, script, style, template, title

### 섹션 콘텐츠 \(Section Conetnt\)

웹 문서의 섹션 영역을 정의하는 요소입니다.  
섹션 콘텐츠는 헤딩과 푸터의 유효범위를 지정함.  
제목과 그 내용을 포함하는 범위를 지정함.

article, aside, nav, section

### 헤딩 콘텐츠 \(Heading Conetnt\)

헤딩 콘텐츠는 섹션\(섹션 콘텐츠나 또는 헤딩 콘텐츠에 의해 암시적으로 마크업 된 영역\)의 헤더를 정의한다.

h1, h2, h3, h4, h5, h6

### 프레이징 콘텐츠 \(Phrasing Conetnt\)

프레이징 콘텐츠는 문장과 텍스트가 관련된 요소입니다.  
프레이징 콘텐츠는 문서의 텍스트이며, 그 텍스트를 단락 내부레벨에서 마크업을 하는 요소임.  
프레이징 콘텐츠가 모여 문단을 구성한다.  
일반적으로 프레이징 콘텐츠 모델 요소를 포함할 수 있는 요소들은 최소 하나의 공백이 아닌 텍스트를 포함하거나 또는 최소 하나의 임베디드 콘텐츠를 포함하여야 한다.

a \(프레이징 콘텐츠만을 포함하는 경우\), abbr, area \(map 요소의 자식요소인 경우\), audio, b, bdi, bdo, br, button, canvas, cite, code, command, datalist, del \(프레이징 콘텐츠을 포함하는 경우\), dfn, em, embed, i, iframe, img, input, ins \(프레이징 콘텐츠만을 포함하는 경우\), kbd, keygen, label, map \(프레이징 콘텐츠만을 포함하는 경우\), mark, math, meter, noscript, object, output, progress, q, ruby, s, samp, script, select, small, span, strong, sub, sup, svg, textarea, time, var, video, wbr, text

### 임베디드 콘텐츠 \(Embedded Conetnt\)

다른 소스를 가져오거나 삽입시키는 컨텐츠와 관련된 요소입니다.  
임베디드 콘텐츠는 다른 리소스\(음악, 영상 등\)를 문서에 삽입하는 콘텐츠나, 문서에 삽입된 다른 형태에서 유래한 콘텐츠를 말한다.  
HTML의 네임스페이스에 속하지 않으면서, 콘텐츠를 포함하고 있지만 메타데이터가 아닌 것들을 임베디드 콘텐츠라 한다. \(SVG등\)  
임베디드 콘텐츠 요소 중 일부는 외부 리소스가 사용이 불가능 할때 사용할 대체 콘텐츠를 갖는다.

audio, canvas, embed, iframe, img, math, object, svg, video

### 인터랙티브 콘텐츠 \(Interactive Conetnt\)

인터랙티브 콘텐츠는 사용자와의 상호작용을 위해 사용되는 콘텐츠이다.

a, audio \(controls 속성이 있으면\), button, details, embed, iframe, img \(usemap 속성이 있으면\), input \(type 속성이 hidden 상태가 아니면\), keygen, label, menu \(type 속성이 toolbar 상태면\), object \(usemap 속성이 있으면\), select, textarea, video \(controls 속성이 있으면\)

위에서 언급하지 않은 요소들은 다음과 같습니다.

## 11.1. 인터랙티브 요소 &lt;details&gt; element

> ### 요약 설명
>
> &lt;details&gt; 요소는 "열림" 상태일 때만 내부 정보를 보여주는 정보 공개 위젯을 생성합니다.  
> 요약이나 레이블은 &lt;summary&gt; 요소를 통해 제공할 수 있습니다.
>
> 정보 공개 위젯은 보통 레이블 옆의 작은 삼각형이 돌아가면서 열림/닫힘 상태를 나타냅니다.  
> &lt;details&gt; 요소의 첫 번째 자식이 &lt;summary&gt; 요소라면, &lt;summary&gt;의 콘텐츠를 위젯의 레이블로 사용합니다.
>
> 즉, 사용자가 직접 조작하여 보거나 숨길 수 있는 부가적인 세부사항\(additional details\)을 명시할 때 사용합니다.  
> &lt;details&gt; 요소는 보통 사용자가 직접 접거나 펼 수 있는 대화형 위젯\(interactive widget\)을 정의할 때 사용되며, 그 안에는 어떠한 종류의 콘텐츠도 포함될 수 있습니다.  
> 이러한 &lt;details&gt; 요소의 콘텐츠는 open 속성이 설정되기 전까지는 화면에 보이지 않습니다.
>
> &lt;summary&gt; 요소는 &lt;details&gt; 요소에서 화면에 보일 제목\(visible heading\)을 명시할 때 사용합니다.  
> 이 제목을 마우스로 클릭함으로써 &lt;details&gt; 요소를 보이도록 할 수도 있고 숨길 수도 있습니다.

#### \[open\] &lt;details open&gt;

요소가 사용자에게 보이도록 펼쳐짐을 명시함.  
상세 정보, 즉 `<details>` 요소의 콘텐츠가 현재 보이는 상태인지 나타냅니다.  
기본값 false는 정보가 보이지 않는다는 뜻입니다.

```text

<!-- 기본예제 -->
<details>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

```text

<!-- 요약 제공 예제 -->
<details>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

```text

<!-- 열려 있는 상태 예제 -->
<details open>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

## **Web Browser Support for details**

* IE _지원 안 함_
* Edge _지원 안 함_
* Chrome _12.0_
* Firefox _49.0_
* Opera _15.0_
* Safari _6.0_

## 참조

* [W3C details specification](https://www.w3.org/TR/html51/semantics.html#the-details-element) 
* [MDN details specification](https://developer.mozilla.org/ko/docs/Web/HTML/Element/details)
* [W3C 문서](https://www.w3.org/TR/html52/dom.html#content-models)
* [MDN 문서](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories)







