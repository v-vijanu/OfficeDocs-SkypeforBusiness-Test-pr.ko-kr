﻿---
title: 'Lync Server 2013: 에지 지원에 대한 DNS 구성'
TOCTitle: 에지 지원에 대한 DNS 구성
ms:assetid: 955493e6-aa29-424d-bb81-1ef87b3b15e3
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg398756(v=OCS.15)
ms:contentKeyID: 49304425
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013에서 에지 지원에 대한 DNS 구성

 

_**마지막으로 수정된 항목:** 2013-02-15_

내부 및 외부 에지 인터페이스(에지 서버 및 역방향 프록시 인터페이스를 모두 포함)에 대해 DNS(Domain Name System) 레코드를 구성해야 합니다. 기본적으로 에지 서버는 도메인에 연결되지 않으며 FQDN(정규화된 도메인 이름)을 갖지 않습니다. 에지 서버는 정규화된 도메인 이름이 아닌 짧은 (컴퓨터) 이름으로만 참조됩니다. 그러나 토폴로지 작성기에서는 짧은 이름이 아닌 FQDN을 사용합니다. 에지 서버의 이름은 토폴로지 작성기에서 사용하는 FQDN과 일치해야 합니다. 이를 위해 DNS 접미사를 정의하고 컴퓨터 이름과 결합하면 필요한 FQDN이 만들어집니다. 컴퓨터 이름에 DNS 접미사를 추가하려면 "도메인에 가입되지 않은 에지 서버에서 컴퓨터 이름에 DNS 접미사를 추가하려면"에 있는 다음 절차를 따르십시오.


> [!NOTE]
> 기본적으로 DNS는 라운드 로빈 알고리즘을 사용하여 쿼리 답변에서 반환되는 리소스 레코드 데이터의 순서를 회전합니다. 답변에는 쿼리하는 DNS 도메인 이름에 대해 동일한 유형의 여러 리소스 레코드가 있습니다. Lync Server 2013 DNS 부하 분산은 DNS 부하 분산 메커니즘의 일부로 DNS 라운드 로빈을 사용합니다. 라운드 로빈 설정이 해제되지 않았는지 확인합니다. Windows 운영 체제를 실행하지 않는 DNS 서버를 사용 중인 경우에는 라운드 로빈 리소스 레코드 순서 지정이 사용하도록 설정되어 있는지 확인합니다.



각 DNS SRV 레코드를 만들고 확인하려면 “ **DNS SRV 레코드를 만들려면** ”의 절차를 따릅니다.외부 사용자 액세스에 필요한 DNS A 레코드를 정의하려면 “ **DNS A 레코드를 만들려면** ”의 절차를 따릅니다. 레코드가 올바르게 구성되고 작동하는지 확인하려면 이 항목의 “ **DNS 레코드를 확인하려면** ”을 참조하십시오. 외부 사용자 액세스를 지원하는 데 필요한 각 레코드에 대한 자세한 내용은 [Lync Server 2013에 대한 DNS 요구 사항 확인](lync-server-2013-determine-dns-requirements.md)을 참조하십시오.

## 도메인에 연결되지 않은 에지 서버의 컴퓨터 이름에 DNS 접미사를 추가하려면

1.  컴퓨터에서 **시작** 을 클릭하고 **컴퓨터** 를 마우스 오른쪽 단추로 클릭한 다음 **속성** 을 클릭합니다.

2.  **컴퓨터 이름, 도메인 및 작업 그룹 설정** 에서 **설정 변경** 을 클릭합니다.

3.  **컴퓨터 이름** 탭에서 **변경** 을 클릭합니다.

4.  **컴퓨터 이름/도메인 변경** 에서 **자세히** 를 클릭합니다.

5.  **DNS 접미사 및 NetBIOS 컴퓨터 이름** 의 **이 컴퓨터의 주 DNS 접미사** 에 내부 도메인의 이름(예: corp.contoso.com)을 입력하고 **확인** 을 세 번 클릭합니다.

6.  컴퓨터를 다시 시작합니다.

## DNS SRV 레코드를 만들려면

1.  해당 DNS 서버에서 **시작** , **제어판** , **관리 도구** 를 차례로 클릭한 다음 **DNS** 를 클릭합니다.
    

    > [!IMPORTANT]
    > 다음과 같이 DNS를 구성해야 합니다. 1) 원격 사용자 및 페더레이션된 파트너의 외부 DSN 조회를 위한 외부 DNS 항목, 2) 경계 네트워크(DMZ, 완충 지역 및 스크린된 서브넷이라고도 함) 내에 있는 에지 서버가 사용할 수 있는 DNS 조회 항목( Lync Server 2013을 실행하는 내부 서버에 대한 A 레코드 및 3 포함), 3) 내부 클라이언트 및 Lync Server 2013 실행 서버에서 조회하기 위한 내부 DNS 항목.



2.  SIP 도메인의 콘솔 트리에서 **정방향 조회 영역** 을 확장하고 Lync Server 2013이 설치된 도메인을 마우스 오른쪽 단추로 클릭합니다.

3.  **다른 새 레코드** 를 클릭합니다.

4.  **리소스 레코드 종류 선택** 에서 **서비스 위치(SRV)** 를 입력한 다음 **레코드 만들기** 를 클릭합니다.

5.  DNS SRV 레코드에 필요한 모든 정보를 제공합니다.

## DNS A 레코드를 만들려면

1.  해당 DNS 서버에서 **시작** , **제어판** , **관리 도구** 를 차례로 클릭한 다음 **DNS** 를 클릭합니다.

2.  SIP 도메인의 콘솔 트리에서 **정방향 조회 영역** 을 확장하고 Lync Server 2013이 설치될 도메인을 마우스 오른쪽 단추로 클릭합니다.

3.  **새 호스트(A)** 를 클릭합니다.

4.  DNS SRV 레코드에 필요한 모든 정보를 제공합니다.

## DNS 레코드를 확인하려면

1.  도메인의 클라이언트 컴퓨터에 로그온합니다.

2.  **시작** 을 클릭한 다음 **실행** 을 클릭합니다.

3.  명령 프롬프트에서 다음 명령을 실행합니다.
    
        nslookup <FQDN edge interface>

4.  FQDN에 대해 적절한 IP 주소로 확인되는 응답이 수신되는지 점검합니다.

## 참고 항목

#### 작업

[호스트되는 Exchange UM과의 통합을 위한 DNS SRV 레코드 만들기](lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md)  

#### 개념

[Lync Server 2013에 대한 DNS 요구 사항 확인](lync-server-2013-determine-dns-requirements.md)
