---
layout: post
title: text-overflow 와 whit-space
date: 2018-08-11
excerpt: 
---
<style>
div {
  display : block;
  width : 100%;
  height : auto;
}
p {
  width: 100%;
}
code {
  width: 100%;
}
</style>

<div>
  <p>
    글자가 너무 길 경우 긴 글자를 width값에 맞게 처리해줄때 사용한다 물론 제이쿼리를 이용해서 바꿀수있지만<br/>
    css로도 바꿀수 있다!<br/>
    
  </p>
  <code>
    text-overflow: ellipsis;
    white-space: nowrap;
  </code>
  우선 이렇게 적용을할때 nowrap을 쓰면 display가 사라지니 block속성을 줘야한다
  <code>
    display: block;
    overflow: hidden;
  </code>
  <p>
    그리고 글자가 width값을 넘어가는 경우 hidden처리를 해주자!
  </p>
</div>
