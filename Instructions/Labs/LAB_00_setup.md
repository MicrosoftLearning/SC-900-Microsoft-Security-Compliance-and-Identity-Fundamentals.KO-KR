---
lab:
  title: 랩 설정
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# 랩: 설정

## WWL 테넌트 - 사용 약관
강사 진행 교육 제공의 일부로 테넌트를 제공하는 경우, 강사 진행 교육에서 실습 랩을 지원하기 위해 테넌트를 사용할 수 있습니다.

테넌트를 실습 랩 외부에서 공유하거나 사용해서는 안 됩니다. 이 과정에서 사용되는 테넌트는 평가판 테넌트이며 클래스가 종료된 후 사용하거나 액세스할 수 없으며 확장판에서도 사용할 수 없습니다.

테넌트를 유료 구독으로 변환해서는 안 됩니다. 이 과정의 일부로 얻은 테넌트는 Microsoft Corporation의 재산으로 유지되며 언제든지 액세스 권한을 획득하고 다시 소유할 수 있는 권리를 보유합니다.

## 랩 시나리오

이 설정 랩은 Microsoft 감사 로그 사용 설정으로 구성됩니다.

**예상 시간:** 5~10분

### 설정 - Microsoft 365 감사 로그를 사용하도록 설정

이 설정 작업에서는 Microsoft 365의 감사 로그 기능을 사용하도록 설정합니다.  설명서에는 감사 로그가 기본적으로 켜져 있다고 나와 있지만 대부분의 랩 테넌트에는 이 기능이 사용하도록 설정되어 있지 않으며 기능을 적용하려면 몇 시간이 걸릴 수도 있습니다.  Microsoft 365에서는 감사 로그를 사용하여 정책 및 분석 인사이트에서 확인된 활동과 사용자 인사이트를 파악하므로, 이 기능을 사용하도록 설정하면 유용합니다.

1. Microsoft Edge를 엽니다. 주소 표시줄에 **admin.microsoft.com**을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다. 그러면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시**를 선택합니다.

1. 관리 센터 아래에서 규정 **준수**를 선택합니다.  새 브라우저 페이지가 열리고 Microsoft Purview 규정 준수 포털 시작 페이지가 표시됩니다.  

1. 왼쪽 탐색 패널의 솔루션 아래에서 **감사**를 선택합니다.  참고: Microsoft 365 Defender 홈 페이지(이전 명칭: Microsoft 365 보안 센터)에서도 감사 기능에 액세스할 수 있습니다.

1. **새 검색** 탭이 선택되어 있는지(밑줄 표시) 확인합니다.

1. 감사 페이지가 표시되면 2~3분 정도 기다립니다.  감사가 사용하도록 설정되어 있지 않으면 페이지 위쪽에 사용자 및 관리자 활동 기록을 시작하라는 파란색 막대가 표시됩니다.  **사용자 및 관리자 활동 기록 시작**을 선택합니다.  조직 설정을 업데이트해야 하는지 확인하라는 메시지가 표시되면 **예**를 선택합니다. 감사가 사용하도록 설정되면 파란색 막대는 사라집니다.  파란색 막대가 없으면 감사가 이미 사용하도록 설정된 것이므로 추가로 작업을 수행할 필요가 없습니다.  PowerShell을 통해서도 감사가 사용하도록 설정되었는지 확인할 수 있습니다. 하지만 이 과정에서는 해당 방법을 설명하지 않습니다.

1. Microsoft 365에서 로그아웃하려면 왼쪽 탐색 패널에서 **홈**을 선택하여 Microsoft Purview 규정 준수 포털 홈 페이지로 돌아옵니다. Microsoft 365 창 오른쪽 위의 물음표 옆 아이콘(원 안에 MA라는 글자가 표시된 아이콘)을 선택하고 **로그아웃**을 선택하여 로그아웃한 후에 브라우저를 닫습니다.

### 검토

이 설정에서 Microsoft 365의 감사 로그 기능을 사용하도록 설정했습니다.
