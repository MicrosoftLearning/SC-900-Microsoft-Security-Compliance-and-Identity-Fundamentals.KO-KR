---
lab:
  title: 랩 설정
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# 랩: Microsoft 365 테넌트 설정

## WWL 테넌트 - 사용 약관
강사 진행 교육 제공의 일부로 테넌트를 제공하는 경우, 강사 진행 교육에서 실습 랩을 지원하기 위해 테넌트를 사용할 수 있습니다.

테넌트를 실습 랩 외부에서 공유하거나 사용해서는 안 됩니다. 이 과정에서 사용되는 테넌트는 평가판 테넌트이며 클래스가 종료된 후 사용하거나 액세스할 수 없으며 확장판에서도 사용할 수 없습니다.

테넌트를 유료 구독으로 변환해서는 안 됩니다. 이 과정의 일부로 얻은 테넌트는 Microsoft Corporation의 재산으로 유지되며 언제든지 액세스 권한을 획득하고 다시 소유할 수 있는 권리를 보유합니다.

## 랩 시나리오

이 설치 랩은 Microsoft 365 테넌트에서 Microsoft 감사 로그 및 파일 모니터링 기능을 사용하도록 설정하는 것으로 구성됩니다.

**예상 시간:** 5~10분

### 설정 - Microsoft 365 감사 로그 및 파일 모니터링을 사용하도록 설정

이 설정 작업에서는 Microsoft 365의 감사 로그 및 파일 모니터링 기능을 사용하도록 설정합니다.  

1. Microsoft Edge를 엽니다. 주소 표시줄에 **`https://admin.microsoft.com`** 을 입력합니다.

1. ALH(권한 있는 랩 호스터)에서 제공한 Microsoft 365 테넌트의 관리자 자격 증명으로 로그인합니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시**를 선택합니다.

1. 관리 센터 아래에서 **보안**을 선택합니다.  새 브라우저 페이지가 열리고 Microsoft Defender 포털 시작 페이지가 표시됩니다.

1. 왼쪽 탐색 패널에서 아래로 스크롤하여 **시스템**을 확장합니다.  확장된 목록에서 **감사**를 선택합니다.  참고: Microsoft Purview 포털을 통해 감사 기능에 액세스할 수도 있습니다.

1. 감사 페이지가 표시되면 1~2분 정도 기다립니다.  감사가 사용하도록 설정되어 있지 않으면 페이지 위쪽에 사용자 및 관리자 활동 기록을 시작하라는 파란색 막대가 표시됩니다.  **사용자 및 관리자 활동 기록 시작**을 선택합니다.  감사가 사용하도록 설정되면 파란색 막대는 사라집니다.  파란색 막대가 없으면 감사가 이미 사용하도록 설정된 것이므로 추가로 작업을 수행할 필요가 없습니다.  "죄송합니다, 활동이 기록되고 있는지 파악하는 데 문제가 있습니다"라는 메시지가 표시되는 경우 페이지를 새로 고쳐 보십시오."라는 메시지가 표시되고 페이지를 새로 고친 후에도 아무런 변화가 없으면 PowerShell을 통해 감사를 사용 설정해야 합니다.
    1. 작업 표시줄에서 파란색 Windows PowerShell 아이콘을 마우스 오른쪽 버튼으로 선택하고 **관리자로 실행**을 선택합니다.
    1. 컴퓨터에 Exchange Online PowerShell 모듈이 설치되어 있는지 확인하려면 **`Get-InstalledModule ExchangeOnlineManagement | Format-List Name,Version,InstalledLocation`**(을)를 입력합니다.  Exchange OnlineManagement의 이름, 버전 및 설치된 위치가 표시됩니다.
    1. 이제 **`Import-Module ExchangeOnlineManagement`**(을)를 입력하여 모듈을 로드합니다.
    1. 연결하려면 **`Connect-ExchangeOnline -UserPrincipalName admin@WWLxZZZZZZ.onmicrosoft.com`**(을)를 입력합니다.  UPN의 경우 랩의 리소스 탭에 있는 관리자 사용자 이름을 입력합니다.
    1. 다시 로그인하라는 메시지가 표시됩니다.  랩의 리소스 탭에 있는 관리 사용자 이름 및 암호를 입력합니다.
    1. 감사를 켜려면 **`Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true`**(을)를 입력합니다. 변경 내용이 적용되는 데 최대 60분이 걸릴 수 있다는 메시지가 표시됩니다.
    1. 변경 내용이 적용되려면 최대 60분이 소요될 수 있지만 **`Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled`**(을)를 입력하면 명령이 수신되었는지 확인할 수 있습니다.  감사를 사용하도록 설정한 경우 UnifiedAuditLogIngestionEnabled 속성은 true 값을 표시합니다.

1. 왼쪽 탐색 패널의 시스템에서 **설정**을 선택합니다.

1. 설정 페이지에서 **클라우드 앱**을 선택합니다.   아래로 스크롤한 다음 **Information Protection**에서 **파일**을 선택합니다.

1. 파일 모니터링을 아직 사용하도록 설정하지 않았다면 **파일 모니터링 사용** 옆의 박스를 선택한 후에 **저장**을 선택해야 합니다.  

1. 그러면 Microsoft 365 테넌트에 대한 랩 설정이 종료됩니다.

### 검토

이 설정에서 Microsoft 365의 감사 로그 및 파일 모니터링 기능을 사용하도록 설정했습니다.
