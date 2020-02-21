# 10.3 프레임셋 문서 구조

&lt;frameset&gt; 요소는 문서의 레이아웃을 구성하기 위해 사용되는 프레임\(frame\)들의 집합을 정의할 때 사용합니다.  
&lt;frameset&gt; 요소는 하나 이상의 &lt;frame&gt; 요소를 포함하며, 각각의 &lt;frame&gt; 요소는 서로 다른 문서를 포함할 수 있습니다.  
&lt;frameset&gt; 요소는 열\(column\)이나 행\(row\)의 개수뿐만 아니라 각 열과 행이 어느 정도의 면적을 차지하고 있는지 퍼센트\(%\)나 픽셀\(pixel\) 단위로 명시합니다.  
  
HTML5에서는 &lt;frameset&gt; 요소를 더 이상 지원하지 않습니다.  
더 이상 지원되지 않는 &lt;frame&gt; 요소를 사용하면서 HTML 유효성 검사를 통과하기 위해서는 다음의 두 가지 방법처럼 DOCTYPE을 선언해야 합니다.  
&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"&gt;  
&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd"&gt;cols 속성 - 픽셀,%,\*프레임셋의 열\(column\)의 개수와 각각의 크기를 명시함.  
HTML5에서는 더 이상 지원하지 않음.rows 속성 - 픽셀,%,\*프레임셋의 행\(row\)의 개수와 각각의 크기를 명시함.  
HTML5에서는 더 이상 지원하지 않음.

```text

<frameset cols="33%,*,33%">
	<frame name="left" src="/html/intro"/>
	<frame name="center" src="/css/intro"/>
	<frame name="right" src="/php/intro"/>
</frameset>
```

