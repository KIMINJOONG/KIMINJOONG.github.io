---
layout: post
title: position속성과float속성
date: 2018-08-04
excerpt: 재미있다!
---
<style>
div, p, ul{
  display: block;
}
  
</style>
<div>
  <p>
  <ul><h2>position : static;</h2></ul>
      <li>모든 태그의 기본 위치 속성값 default값</li>
      <li>이동속성 (left, top, right, bottom) 적용안됌</li>
  </p>
  <p>
    <ul><h2>position : relative;</h2></ul>
    <li>절대좌표 영역으로 출력된 자식 태그와 부모 관계 설정을 위한 속성 (!절대적인 사용이유)</li>
    <li>static(상대좌표)위치에서 이동속성을 적용 할 수 있다.</li>
    <li>absolute이면서 static? <br/>
        1. 움직이는게 가능하기때문<br/>
        2. relative로 이동속성을 쓰지않는다! 왜? <br/>
          -현재 원래 자리 위치에서 이동을 하기때문에! 그럴거면 마진을 사용
    </li>
  </p>
  <p>
    <ul>
      <h2>position : absolute;</h2>
    </ul>
    <li>태그요소를 절대좌표 영역으로 출력하는 위치속성</li>
    <li>left, right, top, bottom 이동속성으로 위치를 지정</li>
  </p>
  <p>
    <ul>position : fixed;</ul>
    <li>브라우저를 기본으로 좌표를 잡는다 부모관계설정이 불가능 위치속성은 적용가능! </li>
  </p>
  <p>
    <ul>
      <h2>z-index</h2>
    </ul>
    <li>절대좌표영역에 출력된 태그의 쌓임순서 (stack lever)을 변경</li>
    <li>값이 클수록 위쪽으로 올라온다.</li>
  </p>
 <p>
  <ul>
    <h2>overflow 속성</h2>
  </ul>
  <li>부모영역을 벗어난 자식태그의 부분을 화면에서 처리하는 속성</li>
 </p>
 <p>
  <ul>
    <h2>float속성과 텍스트 요소</h2>
  </ul>
  <li> float 태그요소 밑으로 텍스트가 침범할 수 없다.</li>
 </p>
 <ul>
  <h2>float와 clear 속성</h2>
 </ul>
 <li> left, right으로 float된 태그를 해제할 때 clear속성을 지정한다</li>
 <li> 해제된 float태그는 밑으로 정렬된다.</li><br/>
 <ul>float와 overflow속성</ul>
 <li>float된 자식태그요소를 가지는 부모태그는 자식태그의 높이값이 지정되지 않는다.</li>
 <li>float된 자식태그요소의 높이값을 부모태그에 지정하기 위해 overflow속성을 지정한다.</li><br/>
 <ul>
  <h2>float속성</h2>
 </ul>
 <li>블록태그를 가로방향으로 할때 가장 많이 쓴다.</li>
 <li>inline-block대신 사용 inline-block은 여백이 자동으로 생기기때문에!</li>
 <li>float일땐 부모한테 overflow : hidden or auto 처리를 해야함 공식! 마치 부모한테 relative를 주는것처럼!</li>
</div>
<div>
  <p>
    헤더 : 메뉴, 로고 등이 들어감<br/>
    푸터 : 사이트의 정보, 주소, 운영업체명, copyright 등<br/>
    컨텐트 : aside, content 등으로 세분화<br/>
    레이아웃의 높이는 main이 결정함 그래서 전체를 감싸고 있는 wrapper는 높이 크기를 auto로 주는것이 현명하다.<br/>
    section의 높이도 article에 의해 결정 auto가 현명
  </p>
</div>
