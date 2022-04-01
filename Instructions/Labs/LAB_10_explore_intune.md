---
lab:
  title: Microsoft Intune 살펴보기
  module: 'Module 3 Lesson 6: Describe the capabilities of Microsoft security solutions: Describe endpoint security with Microsoft Intune'
ms.openlocfilehash: 648343111d82426fe30e1ceeed4e91062649fbcd
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894217"
---
# <a name="lab-explore-microsoft-intune"></a>랩: Microsoft Intune 살펴보기

## <a name="lab-scenario"></a>랩 시나리오

이 랩에서는 Microsoft Endpoint Manager의 Microsoft Intune을 살펴봅니다. 참고: 이 랩 인스턴스에는 엔드포인트나 디바이스가 구성되어 있지 않으므로 이 연습에서는 실제 엔드포인트 정보가 표시되지 않습니다. 즉, 이 연습에서는 Intune에서 제공되는 정보와 해당 정보를 찾을 수 있는 위치만 파악하면 됩니다.  자세한 연습은 연결된 관련 Learn 콘텐츠에 있는 비디오(<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>)를 참조하세요.

**예상 소요 시간:** 10~15분

#### <a name="task-in-this-task-you-will-explore-microsoft-intune-in-microsoft-endpoint-manager"></a>작업: 이 작업에서는 Microsoft Endpoint Manager의 Microsoft Intune을 살펴봅니다.

1. Microsoft Edge를 엽니다. 주소 표시줄에 **admin.microsoft.com** 을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음** 을 선택합니다.
    
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인** 을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예** 를 선택합니다. 그러면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시**, **모든 관리 센터** 를 차례로 선택합니다.

1. 모든 관리 센터 페이지에서 **Endpoint Manager** 을 선택합니다.  새 브라우저 페이지가 열리고 Microsoft Endpoint Manager 관리 센터가 표시됩니다.

1. 왼쪽 탐색 창에서 **대시보드** 를 선택하여 Intune 테넌트의 디바이스 및 클라이언트 앱와 관련된 전반적인 세부 정보를 표시합니다.

1. 왼쪽 탐색 창에서 **디바이스** 를 선택하여 Intune 테넌트에 등록되어 있는 디바이스와 관련된 세부 정보를 표시합니다. 디바이스 - 개요 창에는 다음 상태 및 경고에 대한 요약을 볼 수 있는 여러 탭이 있습니다.
    1. **등록 상태** - 플랫폼 및 등록 오류별로 Intune 등록 디바이스에 대한 세부 정보를 검토합니다.
    
    1. **등록 경고** - 플랫폼별로 할당되지 않은 디바이스에 대한 자세한 내용을 확인합니다.
    1. **준수 상태** - 디바이스, 정책, 설정, 위협 및 보호에 따라 준수 상태를 검토합니다. 또한 이 창에서는 준수 정책을 사용하지 않는 디바이스 목록을 제공합니다.
    1. **구성 상태** - 프로필 배포뿐만 아니라 디바이스 프로필의 구성 상태를 검토합니다.
    1. **소프트웨어 업데이트 상태** - 모든 디바이스 및 모든 사용자에 대한 배포 상태를 시각적으로 표시합니다.

1. 디바이스 - 개요 창에서 **조건부 액세스** 를 선택하여 액세스 정책에 대한 세부 정보를 표시합니다.

1. 왼쪽 탐색 창에서 **디바이스**, **구성 프로필** 을 차례로 선택하여 Intune의 디바이스 프로필 관련 세부 정보를 표시합니다.

1. 왼쪽 탐색 창에서 **디바이스**, **모든 디바이스** 를 차례로 선택하여 Intune 테넌트에 등록된 디바이스 관련 세부 정보를 표시합니다.  여기서는 아무 디바이스도 표시되지 않지만, 이 표를 통해 규정 준수, OS 버전, 마지막 체크 인 날짜 등의 주요 세부 정보를 파악할 수 있습니다.

1. 탐색 창에서 **앱** 을 선택하여 앱 상태 개요를 표시합니다. 이 창에서는 2개 탭을 통해 다음 상태의 요약을 확인할 수 있습니다.
    1. **설치 상태** - 디바이스의 상위 설치 오류뿐만 아니라 설치 오류가 있는 앱을 표시합니다.
    1. **앱 보호 정책 상태** - 플래그가 지정된 사용자뿐만 아니라 앱 보호 정책에 할당된 사용자에 대한 세부 정보를 찾습니다.

1. 앱 - 개요 창에서 **모든 앱** 을 선택하여 Intune에 추가된 앱 목록을 확인합니다.

1. 왼쪽 탐색 창에서 **사용자** 를 선택하여 Intune에 포함한 사용자 관련 세부 정보를 표시합니다. 이러한 사용자는 회사(Contoso)의 인력입니다.

1. 왼쪽 탐색 창에서 **그룹** 을 선택하여 Intune에 포함한 Azure Active Directory(Azure AD) 그룹 관련 세부 정보를 표시합니다.

1. 왼쪽 탐색 창에서 **테넌트 관리** 를 선택하여 Intune 테넌트 관련 세부 정보를 표시합니다.

1. 왼쪽 탐색 창에서 **문제 해결 + 지원**, **문제 해결** 을 차례로 선택하여 특정 사용자의 상태 세부 정보를 확인합니다.

#### <a name="review"></a>검토

이 랩에서는 Microsoft Endpoint Manager의 Microsoft Intune을 살펴보았습니다. 참고: 이 랩 인스턴스에는 엔드포인트나 디바이스가 구성되어 있지 않으므로 이 연습에서는 실제 엔드포인트 정보가 표시되지 않습니다. 즉, 이 연습에서는 Intune에서 제공되는 정보와 해당 정보를 찾을 수 있는 위치만 파악하면 됩니다.  자세한 연습은 연결된 관련 Learn 콘텐츠에 있는 비디오(<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>)를 참조하세요.