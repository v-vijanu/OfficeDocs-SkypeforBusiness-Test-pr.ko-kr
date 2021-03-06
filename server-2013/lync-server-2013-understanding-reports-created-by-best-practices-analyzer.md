﻿---
title: 모범 사례 분석기에서 만든 보고서 이해
TOCTitle: 모범 사례 분석기에서 만든 보고서 이해
ms:assetid: 1386dd6c-7f3e-4da9-905b-cef1468bf14a
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg591344(v=OCS.15)
ms:contentKeyID: 49302879
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 모범 사례 분석기에서 만든 보고서 이해

 

_**마지막으로 수정된 항목:** 2012-10-10_

모범 사례 분석기는 문제를 원활하게 분석 및 확인할 수 있도록 구성된 다양한 유형의 보고서를 제공합니다. 모범 사례 문석기는 오류, 경고, 기타 정보 등의 문제를 식별합니다.

## 보고서

다음의 각 보고서를 표시하면 검색 결과에 액세스할 수 있습니다.

  - **목록 보고서**   목록 보고서는 특정 기준에 따라 구성됩니다. 결과를 클래스, 심각도 또는 문제별로 정렬할 수 있습니다. 예를 들어 결과를 클래스별로 구성하는 경우 디렉터 관련 문제는 보고서의 디렉터 섹션에 포함됩니다. 모든 문제를 볼 수도 있고 정보 항목만 볼 수도 있습니다. 목록 보고서에서는 메모리 등의 특정 항목을 검색할 수 있습니다. 보고서를 인쇄하거나 내보낼 수도 있습니다.

  - **트리 보고서**   트리 보고서는 검색을 실행하는 데 사용되는 규칙 및 검색 실행 시 지정한 기타 옵션을 기준으로 구성됩니다. 예를 들어 테스트 토폴로지 규칙과 관련된 문제는 보고서의 테스트 토폴로지 섹션에 포함됩니다. 모든 문제의 세부 정보를 볼 수도 있고 문제 요약만 볼 수도 있습니다. 트리 보고서에서는 메모리 등의 특정 항목을 검색할 수 있습니다. 보고서를 인쇄하거나 내보낼 수도 있습니다.

  - **기타 보고서**   기타 보고서의 항목으로는 검색에 포함된 작업의 런타임 로그가 포함됩니다. 기타 보고서의 항목에서는 메모리 등의 특정 항목을 검색할 수 있습니다. 보고서를 인쇄하거나 내보낼 수도 있습니다.

## 문제

모범 사례 분석기에서 생성하는 보고서는 환경 검색 중에 식별된 특정 문제를 보여 주며, 여기에는 다음과 같은 유형의 문제가 포함됩니다.

  - **오류**   환경을 변경해야 하는 중대한 문제입니다. 예를 들어 Lync Server 2013 핵심 구성 요소가 설치되어 있지 않으면 오류가 기록됩니다.
    
    오류로 분류된 문제는 보고서에서 빨간색 X 기호로 표시됩니다. 오류는 **목록 보고서** 보기의 경우 **모든 문제** 탭에 표시되고, **트리 보고서** 보기의 경우 **자세히 보기** 및 **요약 보기** 탭에 표시됩니다. 보고서에서 특정 오류를 표시하지 않으려면 보고서에서 해당 오류의 단일 인스턴스 또는 모든 인스턴스에 대해 오류를 표시하지 않도록 지정할 수 있습니다. 이 경우 설정을 변경하여 보고서에 오류가 표시되도록 지정하지 않으면 오류는 **기타 보고서** 보기의 **숨겨진 항목** 탭에만 표시됩니다.

  - **경고**   모범 사례 구현 시 항상 발생하지는 않는 문제입니다. 환경을 변경해야 할 수도 있고 그렇지 않을 수도 있습니다. 즉, 변경할 필요가 없는 특정 설정과 관련된 알려진 문제일 수 있습니다. 예를 들어 서버에서 시작되지 않는 서비스는 경고로 기록됩니다.
    
    경고로 분류된 문제는 보고서에서 노란색 삼각형 경고 기호로 표시됩니다. 경고는 **목록 보고서** 보기의 경우 **모든 문제** 탭에 표시되고, **트리 보고서** 보기의 경우 **자세히 보기** 및 **요약 보기** 탭에 표시됩니다. 보고서에서 특정 오류를 표시하지 않으려면 보고서에서 해당 오류의 단일 인스턴스 또는 모든 인스턴스에 대해 오류를 표시하지 않도록 지정할 수 있습니다. 이 경우 설정을 변경하여 보고서에 경고가 표시되도록 지정하지 않으면 경고는 **기타 보고서** 보기의 **숨겨진 항목** 탭에만 표시됩니다.

  - **정보**   오류 또는 경고로 분류되지 않는 모든 문제를 포함합니다. 예를 들어 Active Directory 도메인 서비스의 Lync Server 2013 Standard Edition 서버 개체 수는 정보 문제로 분류됩니다.
    
    정보 문제는 **목록 보고서** 보기의 경우 **모든 문제** 탭에 표시되고, **트리 보고서** 보기의 경우 **자세히 보기** 탭에 표시됩니다.

Lync Server 2013에서 모범 사례 문석기는 문제를 해결하기 위해 환경을 변경하지 않습니다. 검색에서는 잠재적 문제만 검색하여 각 문제를 해결하는 방법에 대한 정보가 포함된 보고서를 제공합니다.

문제를 클릭하면 설명과 몇 가지 옵션이 특정 문제에 대해 표시됩니다. 그러면 다음과 같은 작업을 수행할 수 있습니다.

  - 문제에 대한 자세한 정보 및 문제 해결 방법 찾기

  - 보고서에 문제가 표시되지 않도록 지정
    
      - 선택한 인스턴스에 대한 문제 표시 중지
    
      - 해당 문제의 모든 인스턴스에 대해 문제 표시 중지
    
    보고서에서 표시되지 않도록 지정한 문제를 확인하려면 **기타 보고서** 보기의 **숨겨진 항목** 탭으로 이동합니다. 이 탭에서 보고서에 문제가 다시 표시되도록 지정할 수 있습니다.

특정 문제를 해결하는 방법에 대한 자세한 내용은 [모범 사례 분석기에서 식별한 문제 분석 및 해결](lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md)을 참조하십시오.

