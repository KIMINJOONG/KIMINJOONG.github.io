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
      dl &gt; .클래스명 ~ dt {} ------> 해당 클래스밑에 있는 li들을 선택 ※본인은 제외 <br/>
      .클래스명, .클래스명 {}   -------> 클래스를 두개 동시에 선택하기 <br/>
      인라인 태그안에 블록태그는 쓰지않는다 ex) &lt;span&gt;안에 div를 선언하지않음 ※단! 블록태그안에 인라인태그는 가능!<br/>
     문단태그안에는 블록태그가 들어 올 수 없습니다. ex) p태그안에 div태그를 넣으면 깨진다 , p태그안에 ul li태그도 안됌 <br/>
     문단태그안에는 인라인태그는 가능하다 ex) p태그안에 span태그 <br/>
     ol &gt; li:ntn-child
     ol &gt; li:nth-of-type(ol 밑에 li태그타입중에 첫번째)
     a[name=a태그에 준 네임값] {} -> name 외에도 id, class, target, title 등 다 들어갈수있음!
      <h2>선택자의 종류</h2>
      <ul>
        <li>* - 전체 선택자</li>
        <li>태그명 - 태그선택자<li>
        <li>.클래스명 - 클래스 선택자</li>
        <li>#아이디   - 아이디 선택자</li>
        <li>부모 > 자식 : 자식선택자</li>
        <li>조성 후손   : 후손선택자</li>
        <li>nth-child  : 구조선택자</li>
        <li>first-child</li>
        <li>nth-of-type()</li>
        <li>태그명[속성=속성값] 속성 선택자</li>
      </ul>
    </div>
  </body>
</html>

