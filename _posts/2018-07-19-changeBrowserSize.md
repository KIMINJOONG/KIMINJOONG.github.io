---
layout: post
title: 2018-07-19 해상도에 맞춘 브라우저 사이즈조절
date:   2018-07-18
excerpt: 검색결과에 따라 동적으로 생성되는 테이블의 사이즈에 브라우저 크기를 맞춰보자
---
<style>
div {
    display: block;
    }
    </style>

<div>
오늘은 검색결과에 따른 팝업브라우저 사이즈를 조절하는 로직을 생각해보았다. 사용자의 편리성을 섬세하게 고려했다..나름 ㅋㅋㅋㅋㅋ우선 필요한 변수가
무엇인지를 생각했고 이것을 하면서 screen.height라던지 Math.abs 절대값을 구하는것 screen.availHeight를 알았다
screen.height = 클라이언트의 해상도 최대 높이값
screen.availHeight = 클라이언트의 작업표시줄을 제외한 최대 높이값
Math.abs(계산식)    = 절대값이 나옴 무조건 양수값
알고리즘을 공부하고있어서 나름의 식을 짜보았다!
    </div>
<table>
    <tr>
        <td>현재브라우저</td>
        <td>이전검색결과높이</td>
        <td>현재검색결과</td>
        <td>전과 현재의 높이차이</td>
        <td>총크기 </td>
    </tr>
    <tr>
        <td>500</td>
        <td>0</td>
        <td>500</td>
        <td>500</td>
        <td>500+500 = 1000</td>
    </tr>
    <tr>
        <td>1000</td>
        <td>500</td>
        <td>300</td>
        <td>200</td>
        <td>1000-200 = 800</td>
    </tr>
    </table>
이전검색결과높이가 현재검색결과 보다 높다면 총크기에서 높이차이의 값을 빼고 현재검색결과가 높으면 높이차이의 값을 더하면 된다!
<div>
<pre style="width:100%;">
<code style="width:100%;">
var vTempTbHeight       = 0; // 이전 검색결과 길이
var vTotalBrowserHegiht = 0; // 전체 팝업 브라우저 길이
var vBrowserHeight      = document.documentElement.clientHeight; //처음시작시 브라우저크기 (고정)
var vResultTbHeight     = 0; //현재 검색결과 높이
var vHeightDifference   = 0; //현재 검색결과 높이와 전에 검색했던 결과높이의 차
    jQuery("#searchResultList").css("height", "100%"); //.css로 800px가 됐을경우 초기화를 위해
    vResultTbHeight   = jQuery("#searchResultList").height();
    vHeightDifference = Math.abs(vResultTbHeight - vTempTbHeight); // 절대값 무조건 양수값
    if (vTempTbHeight == 0 || vTempTbHeight >= screen.availHeight) { //최초로 검색시 or 검색결과값이 클라이언트 해상도 최대값 초과시
        vTotalBrowserHegiht = vBrowserHeight + vResultTbHeight;
    } else {
        vTotalBrowserHegiht = (vTempTbHeight > vResultTbHeight) ? vTotalBrowserHegiht - vHeightDifference : vTotalBrowserHegiht + vHeightDifference;
    }
    if (vTotalBrowserHegiht >= screen.availHeight) {
        jQuery("#searchResultList").css("height", "800px"); //스크롤바 생성을 위해
        vTotalBrowserHegiht  = screen.availHeight;
    } else {
        jQuery("#searchResultList").css("height", "100%");
    }
vTempTbHeight = vResultTbHeight;
window.resizeTo(700, vTotalBrowserHegiht);
</code>
</pre>
<p>
 처음에 screen.availHeight 라는것을 찾아볼 생각도 없었고 대충 screen.height에 -40을 임의로 줘서 적당히 작업표시줄에 안걸리게 맞춰줬었다.
 브라우저에서 동작되는건 다 구현할수있다는것을 간과했고 상사에게 배우게 되어서 절대로 까먹지않기위해 기록을 했다!
</p>
</div>
