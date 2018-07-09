---
layout: post
title: 자바스크립트 id와 name 의 차이점
date:   2018-07-09 23:21:35 +0900
categories: 소스저장소
---
<span>업무 도중 document.getByElementsName("").value = ~~; 로 값을 준적이 있었다
팝업으로 값을 보내야하는데 .submit을 해도 도통 값이 넣어지지 않는 경우가 있었다 분명히 값은 들어있다고 나오는데
자식창에서는 값이 없다니..? 알아본 결과..name은 object NodeList으로 되고 id는 object HTMLInputElement되 있던 것이다!
그도 그럴게 name은 중복으로 주면 허용되니까..흑...이것때문에 삽질을 좀 했다 기록해두고 안잊어버리자ㅏㅏㅏ
</span>
<div class="box alt">
		<div class="row 50% uniform">
			<div class="4u"><span class="image fit"><img src="{{ "/images/namdAndID.PNG" | absolute_url }}" alt="" /></span></div>
		</div>
	</div>
