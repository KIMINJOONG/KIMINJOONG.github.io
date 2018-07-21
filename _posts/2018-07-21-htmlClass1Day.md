---
layout: post
title: 2018-07-21 html 수업 1일째
date: 2018-07-21
excerpt: css 선택자의 실행 순서
image: ""
---
<html>
  <head>
    <meta charset="utf-8"/>
    <title>5-1</title>
  </head>
  <body>
    <div>
         CSS embeded 방식
         CSS 우선순위
         * &lt; 태그 &lt; 클래스 &lt; 아이디 &lt; 인라인 &lt; !important<br/>
        자식 선택자 선택하는법 <br/>
      &lt; style &gt;
        ul &gt; li 를 해주면 ul 하위의 li태그를 선택할 수 있다! 
      &lt; /style &gt; <br/>
      ul &gt; li = 자식 선택자
      ul span    = 후손 선택자
      후손 선택자를 쓰는 경우 자식선택자가 너무 감당이 안됄정도로 많을때<br/>
      ul &gt; li &gt; span  ----------> ul span <br/>
      <h2>형제선택자</h2>
      ul &gt; .클래스명 + li {}  -----> 해당 클래스를 가지고있는 li 태그의 다음번째 li가 선택이 된다. <br/>
      dl &gt; .클래스명 ~ dt {} ------> 해당 클래스밑에 있는 li들을 선택 ※본인은 제외 
    </div>
  </body>
</html>

