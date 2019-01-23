---
layout: post
title: 오늘 배운것 : DOM이란?
date: 2019-01-23
excerpt: DOM이란 무엇일까
image: ""
sitemap :
  changefreq : daily
  priority : 1.0
---
<div>
    <p>
        리액트에서 다음 지도 api를 이용해 사이드프로젝트를 진행하는중이였다...당최 구현을 어떻게 해야될지몰라서<br/>
        찾고찾고 물어물어 이틀만에 구현을 하였다. 문제점은 componentDidMount함수안에 동적으로 다음지도 api를 불러오는 스크립트<br/>
        를 선언해서 그런것같다...그냥 자바스크립트만써서 그런가..리액트에서는 스크립트태그를 어떻게 불러와야할지 구글링을 하였는데<br/>
        알고보니 그게 동적으로 불러오는 구문이였다..위에사람한테 이일을 얘기하니 아직 DOM에대해 정확히 이해를 못해서 그런걸수도 있다고<br/>
        하였기때문에 맞는말 같아서 DOM에 대해 정리를 해보려고한다!
    </p>
</div>
<div>
    <h2>DOM(Document Object Model)이란?</h2>
    <p>브라우저 화면에 보이는 요소를 조작하기 위한 기능으로 가득차있는 각각의 라이브러리라고 덩어리라고 한다.</p>
    <p>자바스크립트를 세분화하면 다음과 같다.</p>
    <ul>
        <li>자바스크립트 코어 문법 : 기본 문법과 구조, 데이터타입, 조건문, 반복문, 함수, 객체, 클래스(프로토타입)등이 포함되있음</li>
        <li>자바스크립트 core 라이브러리 : 자바스크립트에서 기본으로 제공하는 문자열(String), Date, Math, Array, Number,타이머 함수를<br/>
            비롯한 기타 전역함수등이 포함
        </li>
        <li>자바스크립트DOM : 노드(node), 스타일, 속성, 이벤트, 위치 및 크기 등을 다룰수 있는 다양한 기능이 포함되어있음</li>
        <li>자바스크립트BOM(Browser Object Model) : 브라우저와 관련된 window, navagator, Location, History, Document, Screen 객체들이 포함</li>
    </ul>
</div>
<div>
    <h2>D : Document(문서)</h2>
    <p>문서 객체 모델은 문서가 없으면 동작하지 않는다.<br/>
        웹에서 사용할 문서를 만들어 웹 브라우저에 출력하는순간 DOM이 살아 움직이기 시작하는것!<br/>
        그리고 이것은 작성된 웹문서가 객체로 변경되기 때문에 가능한것이다.
    </p>
    <h2>O : Object(객체)</h2>
    <a href="https://webclub.tistory.com/218">출처 : https://webclub.tistory.com/218</a>
</div>
