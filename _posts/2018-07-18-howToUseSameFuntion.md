---
layout: post
title: 2018-07-18 같은 function을 다르게 이용해보자
date:   2018-07-18
excerpt: 굳이 비슷한 fuction을 한개 더 만들지않고 만들어진 function을 이용해보자!
image: ""
---

<div>
사실 이것은 초반에 배웠던 방법인데 잊고 있다가 갑자기 기억나서 글을 올려봅니다
등록폼에서 function을 부르는지 수정폼에서 부르는지 구분을 하기위한 방법
function을 호출할때 1 또는 0 값을 던져준다
해당 function에서 받은 변수가 1일때 0일때 각각의 로직을 태우면 간단하다!
<pre style="width:100%">
  <code>
  function check(type) {
    if (type == 1) {
      console.log("등록폼에서 누름");
    } else {
      console.log("수정폼에서 누름");
    }
  }
  
  등록폼
  &lt;img src="../../button.gif" onclick=check(1);&gt;
  수정폼
  &lt;img src="../../button.gif" onclick=check(0);&gt;
  </code>
</pre>
</div>
