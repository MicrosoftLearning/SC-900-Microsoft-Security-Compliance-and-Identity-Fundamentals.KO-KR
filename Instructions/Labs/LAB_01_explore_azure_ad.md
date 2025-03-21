---
lab:
  title: Microsoft Entra ID 사용자 설정 살펴보기
  module: Describe the function and identity types of Microsoft Entra ID
---

# 랩: Microsoft Entra ID 사용자 설정 살펴보기

이 랩에 해당하는 Learn 학습 내용은 다음과 같습니다.

- 학습 경로: Microsoft Entra의 기능 설명
- 모듈: Microsoft Entra ID의 기능 및 ID 유형 설명
- 단원: ID 유형 설명

## 랩 시나리오

이 랩에서는 Microsoft Entra ID(이전 명칭 Azure Active Directory)에 액세스합니다.  또한 사용자를 만들고 라이선스 추가를 비롯한 여러 가지 설정을 구성합니다.  

**예상 시간:** 30분

### 작업 1

Microsoft 365 구독자로서 이미 Microsoft Entra ID를 사용하고 있습니다.  구체적으로는 Microsoft Entra ID에서 새 사용자를 만드는 방법을 알아보고, 사용자 수준에서 관리할 수 있는 몇 가지 서비스를 살펴봅니다.

1. Microsoft Edge 브라우저를 엽니다. 주소 표시줄에 **`https://admin.microsoft.com`** 입력 후 ALH(권한 있는 랩 호스터)에서 제공한 Microsoft 365 자격 증명을 사용하여 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 ALH에서 제공한 고유 테넌트 ID) **다음**을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인**을 선택합니다.
    1. 랩 호스터에 따라 테넌트에 처음 로그인하는 경우 MFA 등록 프로세스를 완료하라는 메시지가 표시될 수 있습니다. , 화면의 프롬프트에 따라 MFA를 설정합니다.
    1. 로그인하면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. 관리 센터에서 **ID**를 선택합니다(**모두 표시**를 선택한 후 아래쪽으로 스크롤해야 할 수 있음).  새 브라우저 페이지가 열리고 Microsoft Entra 관리 센터 개요 페이지가 표시됩니다.

1. 왼쪽 탐색 창에서 **사용자**를 확장하고 **모든 사용자**를 선택합니다. 테넌트에는 사용자가 이미 구성되어 있습니다.

1. 페이지 맨 위에서 **+ 새 사용자**를 선택한 다음 드롭다운 상자에서 **새 사용자 만들기**를 선택합니다.

1. 그러면 새 사용자 만들기 페이지의 **기본** 탭이 표시됩니다. 다음과 같이 필드에 내용을 입력합니다.
    1. 사용자 계정 이름: **sara**를 입력합니다.

    1. 메일 별칭: 기본값(사용자 계정 이름에서 파생되도록 설정되어 있음)을 그대로 둡니다.

    1. 표시 이름: **Sara Perez**를 입력합니다.

    1. 암호: 암호 자동 생성 확인란 선택을 취소하고 암호 요구 사항을 충족하는 임시 암호를 입력한 후에 적어 둡니다. 후속 작업을 완료하려면 해당 암호가 필요합니다.

    1. 계정 사용: 확인 표시가 된 상태(계정이 사용하도록 설정됨)를 유지합니다.

    1. 페이지 아래쪽에서 **다음: 속성**을 선택합니다.

1. 여기서는 **속성** 탭의 몇 가지 필드를 구성합니다.

    1. 이름: Sara를 입력합니다.

    1. 성: Perez를 입력합니다.

    1. 사용자 유형: 기본값인 **구성원**을 그대로 둡니다. 참고로 드롭다운에서 게스트 선택 옵션도 제공됩니다.

    1. 사용 위치: 사용자의 현재 국가/지역을 선택합니다.  사용 위치 필드는 페이지의 마지막 필드이므로 페이지 아래쪽으로 스크롤해야 표시됩니다.  **참고**: 사용 위치를 올바르게 선택하지 않으면 후속 단계에서 라이선스를 할당할 수 없습니다.

    1. **다음: 할당**을 선택합니다.

1. 그러면 표시되는 **할당** 탭에서 그룹 할당을 추가하고 역할 추가 시에 사용 가능한 옵션을 확인할 수 있습니다.

    1. **그룹 추가**를 선택합니다.

    1. 열리는 창에 사용 가능한 모든 그룹이 표시됩니다.  

    1. 사용 가능한 그룹 목록을 살펴봅니다.  목록에서 **운영**을 선택합니다.  페이지 아래쪽에서 **선택** 단추를 선택합니다.  몇 초 후에 운영 그룹이 할당 페이지에 표시됩니다.

    1. 페이지 위쪽에서 **+ 역할 추가**를 선택합니다.  열리는 창에 사용 가능한 모든 디렉터리 역할이 표시됩니다.  사용 가능한 옵션만 확인하고 새 역할은 추가하지 마세요.  디렉터리 역할 페이지 오른쪽 위에서 **X**를 선택하여 이 페이지를 닫습니다.
    1. 페이지 아래쪽에서 **검토 + 만들기**를 선택합니다. 설정의 요약이 표시됩니다.  페이지 아래쪽에서 **만들기**를 선택합니다.

1. 그러면 사용자 페이지가 다시 표시됩니다.  잠시 후에 Sara Perez가 표시됩니다.  페이지 위쪽에서 **새로 고침** 아이콘을 선택해야 할 수도 있습니다.

1. 사용자 목록에서 만든 사용자인 **Sara Perez**를 선택합니다.  **개요** 페이지가 열립니다.

1. 사용자와 관련하여 구성할 수 있는 다양한 옵션이 왼쪽 탐색 패널에 표시됩니다. 사용 가능한 옵션을 확인합니다.

1. 왼쪽 탐색 패널에서 **라이선스**를 선택합니다.  이 사용자에 대한 라이선스 할당이 없는 것을 확인하고 "라이선스 할당 추가, 제거 및 다시 처리는 M365 관리 센터 내에서만 할 수 있습니다."라는 경고 아이콘도 참고합니다.  다음 작업에서 수행할 예정입니다.  참고: 사용 위치를 구성한 경우에만 라이선스를 할당할 수 있습니다. 사용 위치를 설정하지 않았다면 지금 해당 단계로 돌아갑니다.

### 작업 2

이 작업에서는 Microsoft 365 관리 센터를 사용하여 방금 만든 사용자에게 라이선스를 할당합니다.

1. 브라우저 탭을 열고 **홈 - Microsoft 365 관리 센터**로 이동합니다.

1. 왼쪽 탐색 패널의 사용자에서 **활성 사용자**를 선택합니다.  사용자 목록에서 **Sara Perez**를 선택합니다.  사용자에 대한 정보를 보여주는 창이 열립니다.  

    1. **라이선스 및 앱** 탭을 선택합니다.
    1. 나열된 각 라이선스에 대해 사용 가능한 라이선스 수가 표시됩니다.  사용 가능한 Microsoft 365 E5 라이선스가 없으므로(이미 다른 사용자에게 할당됨) ** Microsoft Power Apps 개발자** 및 **Microsoft Power Automate Free** 옆에 있는 확인란을 선택하여해당 라이선스를 할당합니다.
    1. **변경 내용 저장**을 선택합니다. 화면 오른쪽 위에 라이선스가 정상적으로 할당되었다는 알림이 표시됩니다.
    1. 페이지 오른쪽 위에서 **X**를 선택하여 페이지를 닫습니다.

1. 왼쪽 탐색 패널이나 화면 왼쪽 위(이동 경로)에서 **홈**('Sara Perez | 라이선스' 아래에 있음)을 선택하여 Microsoft Entra 관리 센터로 돌아옵니다.

1. 사용자에게 라이선스를 성공적으로 할당했습니다.

1. 열려 있는 모든 브라우저 탭에서 로그아웃합니다. 화면 오른쪽 위의 이메일 주소 옆에 있는 사용자 아이콘을 선택한 후 **로그아웃**을 선택하여 로그아웃합니다. 그런 다음 브라우저 창을 모두 닫습니다.

### 작업 3

이 작업에서는 Sara Perez로 처음 로그인합니다.

1. Microsoft Edge를 엽니다.

1. 주소 표시줄에 **https://login.microsoft.com**을 입력합니다.

1. **sara@WWLxZZZZZ.onmicrosoft.com**으로 로그인합니다. 여기서 ZZZZZZ는 ALH에서 제공한 고유 테넌트 ID입니다.
1. 이전 작업에서 설정한 임시 암호를 입력합니다.

1. 그러면 암호를 업데이트하라는 메시지가 표시됩니다. 현재 암호 필드에 이전 작업에서 설정한 임시 암호를 입력합니다.

1. 새 암호 필드에 새 암호를 입력하고 확인을 위해 새 암호를 한 번 더 입력한 다음 **로그인**을 선택합니다.  SSPR 관련 후속 랩 연습에서 필요하므로 새 암호를 적어 둡니다.

1. Sara Perez로 로그인하는 것은 이번이 처음이므로 MFA를 설정하라는 메시지가 표시될 수 있습니다. 화면의 프롬프트에 따라 MFA를 설정합니다.

1. 이제 Sara의 Microsoft 계정에 성공적으로 로그인되었습니다.  이전 작업에서 할당한 Sara의 라이선스는 Power Automate Free 및 개발자용 Power Apps로만 제한되었으며 E5 라이선스는 포함되지 않았습니다.

1. Microsoft 365 창 오른쪽 위의 물음표 옆 아이콘(원 안에 SP라는 글자가 표시된 아이콘)을 선택하고 **로그아웃**을 선택하여 로그아웃한 후에 브라우저를 닫습니다.

### 검토

이 랩에서는 Microsoft Entra ID의 초기 탐색을 시작했습니다. Microsoft 365 구독자는 Microsoft Entra ID를 자동으로 사용하므로, Microsoft 365 관리 포털이나 Azure Portal을 통해 Microsoft Entra ID 기능과 서비스에 액세스할 수 있음을 확인했습니다.  원하는 방식을 사용하면 되며, 최종적으로는 같은 페이지가 표시됩니다.  또한 새 사용자를 만드는 프로세스와 사용자를 할당할 수 있는 그룹, 역할의 사용 가능성, 사용자 라이선스 할당 등 구성할 수 있는 다른 설정도 살펴보았습니다.
