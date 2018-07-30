---
layout: post
title: 메이븐을 추가하고 bean을 넣는데 클래스가 없다??
date: 2018-07-28
excerpt: 아니이럴수가?!
image: ""
---

<div style="display:block">
  <p>
    어느날, 혼자 프로젝트를 하는도중 spring ajax json 설정하는법이 필요해서 인터넷 사이트를 뒤져보았드아
  </p><br/>
  
  참조한 사이트 : <a href="http://isntyet.tistory.com/24">http://isntyet.tistory.com/24</a>
  <p>
    근데 dispatcherservlet.xml(내꺼는 servlet.xml)에서 bean 등록을 할때 클래스를 찾지 못하는 오류가 생겨서 당황해버렸다! <br/>
    도대체 왜 오류를 못찾는지 메이븐을 다시 받아보고 버전을 올려보고 낮춰보고 별의 별짓을 다해본것같다...<br/>
    그러다가 회사의 상사한테 여쭤봤는데 jar파일 구조를 보라고 했다 spring.web.servlet.view.json~~어쩌고 이런 경로가 jar파일 안에 존재하는지
    그 얘기를 듣고 눈이 번쩍했다 ㅋㅋㅋ다시는 까먹으면 안돼겠다 jar를 뜯어볼생각은 1도 안해봤는데 앞으로 오류가 난다면 jar파일도 뜯어보고 뜯을 수
    있는건 전부 다 뜯어봐야겠다!
  </p>
  
</div>
<div style="block">
  한줄 요약 : jar를 뜯어서 해당 경로를 타고들어가 class가 존재하는지 안하는지 확인해보자!
</div>
