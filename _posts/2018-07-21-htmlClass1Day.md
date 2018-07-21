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
    <style>
      /* CSS embeded 방식
         CSS 우선순위
         * < 태그 < 클래스 < 아이디 < 인라인 < !important

      */
      * {
        color: orange;
      }
      h1 {
        color: blue;
      }
      .hello {
        color: green !important;
      }
      #hello {
        color: red;
      }
      #hello2 {
        color: yellow;
      }
    </style>
  </head>
  <body>
    <div>
      CSS란? Cascading Style Sheet의 약자이다.<br/>
      Cascading : ㄱ<br/>
                   h1 ㄱ<br/>
                       class ㄱ<br/>
                              id<br/>

      CSS 우선순위<br>
      * &lt; 태그 &lt; 클래스 &lt; 아이디 &lt; 인라인(태그안에 직접 스타일을 주는것) &lt; !important<br/>

    </div>
    <h3>1.CSS 기초</h3>
    <h1>안녕하세요.</h1>
    <h1 class="hello">안녕하세요.</h1>
    <h1 id="hello">안녕하세요.</h1>
    <h1 class="hello" id="hello2" style="color:magenta;">안녕하세요.</h1>
    <h1>안녕하세요.</h1>

  </body>
</html>

