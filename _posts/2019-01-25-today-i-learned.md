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
    <h2>톰캣과 스프링</h2>
    <p>
        톰캣을 스타트하면 톰캣스타트리스너를 먼저 실행시키고 스프링을 실행함<br/>
        스프링을 실행하면 그때 application-context.xml을 읽어서 bean을 등록함(bean에 등록되있는 클래스를 전부 메모리 위에 전부 올린다는뜻)<br/>
        그렇기때문에 톰캣스타트리스너에서 서비스를 부르든 di를 하든 뭘하는 null이 뜰수밖에없다.
        왜냐? 스프링 실행전 즉 .xml을 읽지도않았으니까 메모리에 당연히 올라가있지않으니 못읽는다!
    </p>
    <h2>스레드를 상속받았을경우</h2>
    <p>
        .xml에 bean으로 등록해서 이클래스에서 다른서비스를 쓴다고 선언을 해둬도 의존주입이 불가능함<br/>
        주의! 그럴때는 get메소드로 들고오면됌 service든 dao든 뭐든 set이 있으면 get도 있다는걸 잊지말자!
    </p>
</div>
