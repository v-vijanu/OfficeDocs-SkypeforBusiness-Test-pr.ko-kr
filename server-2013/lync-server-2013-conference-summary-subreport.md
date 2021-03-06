﻿---
title: 전화 회의 요약 하위 보고서
TOCTitle: 전화 회의 요약 하위 보고서
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/JJ204779(v=OCS.15)
ms:contentKeyID: 49303198
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 전화 회의 요약 하위 보고서

 

_**마지막으로 수정된 항목:** 2015-03-09_

전화 회의 요약 하위 보고서에서는 실패한 전화 회의 세션에 대한 전반적인 정보를 제공합니다. 이와 같은 실패한 세션은 세션 유형(회의 센터 세션 및 MCU 세션)별로 세분화됩니다.

## 필터

필터를 사용하면 여러 방식으로 반환된 데이터를 보거나 보다 세부적으로 대상화된 데이터 집합을 반환할 수 있습니다. 다음 표에서는 전화 회의 요약 하위 보고서에 사용할 수 있는 필터를 보여 줍니다.

### 전화 회의 요약 하위 보고서 필터

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>이름</th>
<th>설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>시작</strong></p></td>
<td><p>시간 범위의 시작 날짜/시간입니다. 시간별 데이터를 보려면 다음과 같이 시작 날짜 및 시간을 입력합니다.</p>
<p>2012/7/7 오후 1:00</p>
<p>시작 시간을 입력하지 않으면 보고서가 자동으로 지정된 날짜의 오전 12시부터 시작됩니다. 일별 데이터를 보려면 날짜만 입력합니다.</p>
<p>2012/7/7</p>
<p>주 또는 월별로 보려면 데이터를 보려는 해당 주 또는 월에 속하는 날짜를 입력합니다. 주 또는 월의 첫 번째 날짜를 입력할 필요가 없습니다.</p>
<p>2012/7/3</p>
<p>주는 항상 일요일부터 토요일까지로 실행됩니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>종료</strong></p></td>
<td><p>시간 범위의 종료 날짜/시간입니다. 시간별 데이터를 보려면 다음과 같이 종료 날짜 및 시간을 입력합니다.</p>
<p>2012/7/7 오후 1:00</p>
<p>종료 시간을 입력하지 않으면 보고서가 자동으로 지정된 날짜의 오전 12시에 종료됩니다. 일별 데이터를 보려면 날짜만 입력합니다.</p>
<p>2012/7/7</p>
<p>주 또는 월별로 보려면 데이터를 보려는 해당 주 또는 월에 속하는 날짜를 입력합니다. 주 또는 월의 첫 번째 날짜를 입력할 필요가 없습니다.</p>
<p>2012/7/3</p>
<p>주는 항상 일요일부터 토요일까지로 실행됩니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>풀</strong></p></td>
<td><p>등록자 풀 또는 에지 서버의 FQDN(정규화된 도메인 이름)입니다. 개별 풀을 선택하거나 <strong>[모두]</strong>를 클릭하여 모든 풀에 대한 데이터를 봅니다. 이 드롭다운 목록은 데이터베이스의 레코드에 따라 자동으로 채워집니다.</p></td>
</tr>
</tbody>
</table>


## 메트릭

다음 표에서는 전화 회의 요약 하위 보고서에서 제공되는 정보를 보여 줍니다.

### 전화 회의 요약 하위 보고서 메트릭

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>이름</th>
<th>이 항목에 대한 정렬 가능 여부</th>
<th>설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>총 전화 회의</strong></p></td>
<td><p>아니요</p></td>
<td><p>진행된 총 전화 회의 수입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>총 전화 회의 세션</strong></p></td>
<td><p>아니요</p></td>
<td><p>총 전화 회의 세션 수입니다. 전화 회의 하나에 여러 세션이 포함될 수 있습니다. 예를 들어 하나의 전화 회의가 회의 센터 세션과 MCU 세션을 둘 다 포함할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>전체 세션 실패율</strong></p></td>
<td><p>아니요</p></td>
<td><p>실패한 모든 전화 회의의 비율입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>회의 센터 세션</strong></p></td>
<td><p>아니요</p></td>
<td><p>회의 센터 세션의 총 수입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>회의 센터 실패율</strong></p></td>
<td><p>아니요</p></td>
<td><p>실패한 회의 센터 세션의 비율입니다.</p></td>
</tr>
<tr class="even">
<td><p>MCU 세션</p></td>
<td><p>아니요</p></td>
<td><p>MCU 세션의 총 수입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MCU 실패율</strong></p></td>
<td><p>아니요</p></td>
<td><p>실패한 MCU 세션의 비율입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>형식별 MCU 세션</strong></p></td>
<td><p>아니요</p></td>
<td><p>형식별(예: IM 회의)로 그룹화된 MCU 세션의 총 수입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>형식별 실패율</strong></p></td>
<td><p>아니요</p></td>
<td><p>형식별(예: IM 회의)로 그룹화된 실패한 MCU 세션의 비율입니다.</p></td>
</tr>
</tbody>
</table>

