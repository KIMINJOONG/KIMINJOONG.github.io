---
layout: post
title: 2018-07-17 클릭한 td의 색깔을 변경해보자
date:   2018-07-17
excerpt: 임시변수를 활요하자!
image: ""
---

<div>
오늘은 내가 클릭한 td의 색깔을 바꿔야하는 일이 생겼다.
처음엔 생성되는 td에 아이디값을 1,2,3,4로 줘서 for문을 td개수만큼 돌면서 내가 클릭한 값이랑 일치하면 색이 변하는걸 생각하였다.
근데 이것은 엄청 비효율적이다 만약에 td가 30개면 클릭한번 할 때마다 30번을 도는것이 아닌가!!!그래서 과장님의 힌트를 듣고 임시변수를 활용하여
    만들어 보았다!!! 
    <font color="red">(※vCollection은 저번에 배웠던 map형식으로 만들어져있는 변수이다!)</font>
<pre style="width:100%;">
<code>
function chgTrColor(vCollection){
    if (vTempChkRow != vCollection.chkRow) {
        if (vTempChkRow != -1) {
            document.getElementById("tr" + vTempChkRow).style.background = '#ffffff';
        }
        document.getElementById("tr" + vCollection.chkRow).style.background = 'skyblue';
        vTempChkRow = vCollection.chkRow;
        resizeTo(855, 748);
    } else {
          document.getElementById("tr" + vCollection.chkRow).style.background = '#ffffff';
          resizeTo(634, 748);
          vTempChkRow = -1;
      }
</code>
</pre>
</div>
