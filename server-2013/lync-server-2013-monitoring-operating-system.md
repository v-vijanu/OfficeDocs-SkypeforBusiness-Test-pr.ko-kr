﻿---
title: 'Lync Server 2013: 운영 체제 모니터링'
TOCTitle: 운영 체제 모니터링
ms:assetid: 72406d3e-54c8-4796-8d6d-2144a5b6f030
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Dn720918(v=OCS.15)
ms:contentKeyID: 62240120
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013의 운영 체제 모니터링

 

_**마지막으로 수정된 항목:** 2015-01-26_

Lync Server 2013에서 모든 서버 및 구성 요소의 성능을 모니터링해야 합니다. 가장 중요한 구성 요소 중 하나는 운영 체제 자체입니다. Lync Server 2013은 다음과 같은 운영 체제의 x64 버전을 지원합니다.

  - Windows Server 2008 R2

  - Windows Server 2012 및 Windows Server 2012 R2

운영 체제를 모니터링하는 가장 확실한 방법은 Windows Server 운영 체제 관리 팩을 사용하는 것입니다. 이를 통해 Windows Server 2012, Windows Server 2012 R2, Windows Server 2008 R2를 실행하는 컴퓨터의 성능, 상태, 가용성과 같은 기본적인 모니터링을 수행할 수 있습니다.

이러한 관리 팩은 주요 이벤트 및 성과 지표에 대한 검색, 경고, 자동 응답을 통해 문제 해결에 소요되는 시간을 줄이고 Windows Server 운영 체제를 실행하는 시스템의 전반적인 가용성 및 성능을 향상시킵니다.

System Center Operations Manager와 관련된 Windows Server 관리 팩과 별도로 다음과 같은 시스템 도구 및 리소스를 사용하여 운영 체제 버전에 따라 운영 체제의 상태를 모니터링할 수 있습니다.

## Windows Server 2008 R2

Windows Server 2008 R2에는 관리자의 기본 운영 체제 모니터링 및 관리에 도움이 되는 다음과 같은 추가 기능 및 도구가 포함되어 있습니다.

  - **Windows 리소스 모니터**는 프로세스 및 서비스에서 시스템 리소스가 어떻게 사용되는지를 파악할 수 있게 해주는 강력한 도구입니다. 리소스 모니터를 사용하면 리소스 사용량을 실시간으로 모니터링할 수 있을 뿐 아니라, 응답하지 않는 프로세스를 분석하고, 파일을 사용 중인 응용 프로그램을 식별하고, 프로세스 및 서비스를 제어하는 데에도 도움이 될 수 있습니다.

  - **RAC(Reliability Analysis Component)**는 시스템 사용 및 안정성에 대한 세부적인 환경 정보를 제공하는 기본 에이전트입니다. 이 정보는 Portable Readers Systems에서 사용할 수 있도록 WMI 인터페이스를 통해 노출됩니다. WMI 인터페이스를 통해 RAC(Reliability Analysis Component)를 노출함으로써 개발자는 응용 프로그램을 모니터링 및 분석하고 안정성과 성능을 향상시킬 수 있습니다.

  - **Windows Server 2008 R2**는 기본 제공 RAC(Reliability Analysis Component)를 사용해 안정성 인덱스를 계산하여 시간대별 전체 시스템 사용 및 안정성에 대한 정보를 제공합니다. RAC(Reliability Analysis Component)는 또한 Windows 업데이트 및 응용 프로그램 설치와 같이 안정성에 영향을 줄 수 있는 시스템에 대한 모든 주요 변경 사항을 지속적으로 추적합니다.

## Windows Server 2008 Windows 안정성 및 성능 모니터

Windows 안정성 및 성능 모니터는 성능 로그 및 경고, 서버 성능 관리자, 시스템 모니터를 포함한 이전 독립 실행형 도구의 기능을 결합하는 MMC 스냅인입니다. 여기에는 성능 데이터 수집 및 이벤트 추적 세션을 사용자 지정하기 위한 그래픽 인터페이스가 제공됩니다.

또한 시스템에 대한 변경 사항을 추적하여 시스템 안정성의 변경 사항과 비교하고 이들의 관계를 그래픽으로 나타내는 MMC 스냅인인 안정성 모니터도 포함되어 있습니다.

## Windows 안정성 및 성능 모니터

Windows 안정성 및 성능 모니터는 성능 로그 및 경고, 시스템 모니터, 서버 성능 관리자와 같은 일부 이전 독립 실행형 도구의 기능을 결합할 뿐 아니라 다음과 같은 몇 가지 새로운 기능을 Windows Server 2008 및 Windows Server 2008 R2에 제공하기도 합니다.

  - 데이터 수집기 집합

  - 자원 보기

  - 안정성 모니터

  - 로그를 만들기 위한 마법사 및 템플릿

**데이터 수집기 집합**은 데이터 수집기를 다양한 성능 모니터링 시나리오에 사용하기 위해 재사용 가능 요소로 그룹화합니다. 데이터 수집기 그룹을 데이터 수집기 집합으로 저장한 후에는 단일 속성 변경을 통해 예약과 같은 작업을 전체 집합에 적용할 수 있습니다. Windows 안정성 및 성능 모니터에는 시스템 관리자가 서버 역할 또는 모니터링 시나리오에 관련된 성능 데이터 수집을 즉시 시작하는 데 도움이 되는 기본 데이터 수집기 집합 템플릿이 포함되어 있습니다.

Windows 안정성 및 성능 모니터 홈페이지는 새 **자원 보기** 화면으로, CPU, 디스크, 네트워크, 메모리 사용의 실시간 그래픽 개요를 제공합니다. 시스템 관리자는 모니터링되는 이러한 각 요소를 확장하여 어느 프로세스에 어느 리소스가 사용되고 있는지를 식별할 수 있습니다. 이전 버전의 Windows에서는 이 실시간 프로세스별 데이터를 작업 관리자에서 제한된 형태로만 확인할 수 있었습니다.

**안정성 모니터**는 예기치 않은 문제로 인해 시스템의 안정성이 저하되었는지를 나타내는 시스템 안정성 인덱스를 계산합니다. 시간대별 안정성 인덱스 그래프를 통해 문제가 발생하기 시작한 날짜를 빠르게 식별할 수 있습니다. 관련된 시스템 안정성 보고서에는 안정성 저하의 원인을 해결하는 데 도움이 되는 세부 정보가 제공됩니다. 시스템에 대한 변경 사항(응용 프로그램 설치 또는 제거, 운영 체제 업데이트 또는 드라이버 추가/수정)과 오류(응용 프로그램 오류, 운영 체제 작동 중지 또는 하드웨어 오류)를 나란히 표시하여 살펴보면 문제 해결 방안을 빠르게 마련할 수 있습니다.

로그 파일에 카운터를 추가하고 해당 시작, 중지, 기간을 예약하는 작업을 이제 **마법사 인터페이스**에서 수행할 수 있습니다. 또한 이 구성을 템플릿으로 저장하면 시스템 관리자가 다른 컴퓨터에서 데이터 수집기 선택 및 예약 프로세스를 반복하지 않고 동일한 로그를 수집할 수 있습니다. 성능 로그 및 경고 기능은 모든 데이터 수집기 집합에 사용할 수 있도록 Windows 안정성 및 성능 모니터에 통합되었습니다.

