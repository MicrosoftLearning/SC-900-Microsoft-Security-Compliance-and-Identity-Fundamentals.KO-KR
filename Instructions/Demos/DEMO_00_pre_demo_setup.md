---
Pre-Demo Setup:
    title: '데모 설정'
---

# 데모 전 설정

### 설정 1부 - Azure Pass 사용
이 설정 작업에서는 Microsoft 365 테넌트와 같은 자격 증명을 통해 Azure Pass를 사용합니다.  그러면 Microsoft 365와 Azure 간을 이동하면서 작업할 때 더욱 원활한 환경을 이용할 수 있습니다.

1. 브라우저 창이 열려 있으면 모든 브라우저를 닫는 것이 좋습니다.

1. Microsoft Edge 아이콘을 마우스 오른쪽 단추로 클릭하고 **새 InPrivate 창**을 선택하여 새 InPrivate 브라우저 세션을 엽니다. 기타 

1. 주소 표시줄에 **www.microsoftazurepass.com** 을 입력합니다.  

1. **시작** 단추를 선택하여 시작합니다.

    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 이메일을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다.
    1. 올바른 이메일 주소가 표시되면 **Microsoft 계정 확인**을 선택합니다.
    1. 프로모션 코드 상자에 프로모션 코드를 입력하고 **프로모션 코드 적용**을 클릭합니다.  
    1. "내 프로필" 페이지에서 기본 정보를 모두 그대로 두고 **구독 계약, 제안 세부 정보 및 개인정보처리방침에 동의합니다.** 를 선택한 후에 **등록**을 선택합니다.
    1. 설문 조사 창이 열리면 **X**를 선택하여 해당 창을 닫아도 되고 설문 조사에 응한 후에 **제출**을 선택해도 됩니다.

1. 계정을 활성화하려면 몇 분 정도 걸릴 수 있습니다.  계정이 활성화되면 Azure Portal 홈 페이지로 이동됩니다. Microsoft Azure 시작 창이 열리면 **나중에**를 선택합니다. "개인 설정된 권장 사항으로 클라우드 워크로드를 최적화하세요"라는 메시지가 포함된 팝업 창이 표시될 수 있습니다. 그러면 해당 창의 오른쪽 위에서 **X**를 선택합니다.

1. 다음 데모에서 Azure Portal을 다시 사용할 것이므로 브라우저 탭에 Azure Portal 홈 페이지를 열어 두세요.

### 설정 2부 - Microsoft 365 감사 로그를 사용하도록 설정
이 설정 작업에서는 Microsoft 365의 감사 로그 기능을 사용하도록 설정합니다.  설명서에는 감사 로그가 기본적으로 설정된다고 나와 있지만, 대다수 랩 테넌트에서는 이 기능이 사용하도록 설정되어 있지 않으며 기능을 적용하려면 몇 시간이 걸릴 수도 있습니다.  Microsoft 365에서는 감사 로그를 사용하여 정책 및 분석 인사이트에서 확인된 활동과 사용자 인사이트를 파악하므로, 이 기능을 사용하도록 설정하면 유용합니다.

1. Microsoft Edge를 엽니다. 주소 표시줄에 **admin.microsoft.com**을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예**를 선택합니다. 그러면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시**를 선택합니다.

1. 관리 센터 아래에서 **규정 준수**를 선택합니다.  새 브라우저 페이지가 열리고 Microsoft 365 규정 준수 센터 시작 페이지가 표시됩니다.  

1. Microsoft 365 규정 준수 센터의 왼쪽 탐색 패널에서 **모두 표시**를 선택합니다.

1. 왼쪽 탐색 패널의 솔루션 아래에서 **감사**를 선택합니다.  참고: Microsoft 365 Defender 홈 페이지에서도 감사 기능에 액세스할 수 있습니다.

1. **검색** 탭이 선택되어 있는지(밑줄이 표시되어 있는지) 확인합니다.

1. 감사 페이지가 표시되면 2~3분 정도 기다립니다.  감사가 사용하도록 설정되어 있지 않으면 페이지 위쪽에 사용자 및 관리자 활동 기록을 시작하라는 파란색 막대가 표시됩니다.  **사용자 및 관리자 활동 기록 시작**을 선택합니다.  감사가 사용하도록 설정되면 파란색 막대는 사라집니다.  파란색 막대가 없으면 감사가 이미 사용하도록 설정된 것이므로 추가로 작업을 수행할 필요가 없습니다.

1. 왼쪽 탐색 패널에서 **홈**을 선택하여 Microsoft 365 규정 준수 센터 홈 페이지로 돌아옵니다.

### 복습

이 설정에서는 Microsoft 365 테넌트와 같은 자격 증명을 통해 Azure Pass를 사용했습니다.  그리고 Microsoft 365의 감사 로그 기능을 사용하도록 설정했습니다.

