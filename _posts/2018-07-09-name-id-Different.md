---
layout: post
title: 자바스크립트 id와 name 의 차이점
---

업무 도중 document.getByElementsName("").value = ~~; 로 값을 준적이 있었다
팝업으로 값을 보내야하는데 .submit을 해도 도통 값이 넣어지지 않는 경우가 있었다 분명히 값은 들어있다고 나오는데
자식창에서는 값이 없다니..? 알아본 결과..name은 object NodeList으로 되고 id는 object HTMLInputElement되 있던 것이다!
그도 그럴게 name은 중복으로 주면 허용되니까..흑...이것때문에 삽질을 좀 했다 기록해두고 안잊어버리자ㅏㅏㅏ


![namdandid](https://user-images.githubusercontent.com/34826306/42425597-71387d0c-835a-11e8-9270-0547b08b3faf.PNG)
<div>
<span class="image left"><img src="{{ "/images/namdAndID.png" | absolute_url }}" alt="" /></span>
</div>
