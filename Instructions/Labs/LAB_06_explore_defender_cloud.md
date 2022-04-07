---
lab:
  title: 클라우드용 Microsoft Defender 살펴보기
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: 208e11a7e82497fbb900b4fa024fb6fb367d458e
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894225"
---
# <a name="lab-explore-microsoft-defender-for-cloud"></a>랩: 클라우드용 Microsoft Defender 살펴보기

## <a name="lab-scenario"></a>랩 시나리오
이 랩에서는 클라우드용 Microsoft Defender를 살펴보고 조직의 보안 태세 개선을 위해 Azure 보안 점수를 사용하는 방법을 알아봅니다.

**예상 소요 시간:** 30분

#### <a name="task-1-in-this-task-you-will-take-a-brief-tour-of-microsoft-defender-for-cloud"></a>작업 1: 이 작업에서는 클라우드용 Microsoft Defender를 간단하게 살펴봅니다.
1.  Microsoft Edge를 엽니다. 주소 표시줄에 **portal.azure.com** 을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음** 을 선택합니다.
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인** 을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예** 를 선택합니다.

1. 화면의 왼쪽 위 모서리의 Microsoft Azure 옆에 있는 포털 표시 메뉴 아이콘(햄버거 아이콘이라고도 하는 세 개의 가로줄)을 선택한 다음, 왼쪽 탐색 패널에서 즐겨찾기에서 **클라우드용 Microsoft Defender** 를 선택합니다.  즐겨찾기에 나열되지 않은 경우 검색 상자에 **클라우드용 Microsoft Defender** 를 입력한 다음 결과 목록에서 **클라우드용 Microsoft Defender** 를 선택합니다.

1. 클라우드용 Microsoft Defender 개요 페이지에서 제공하는 정보를 확인합니다.  

1. 제한된 정보만 확인 가능함을 나타내는 파란색 정보 상자가 페이지 위쪽에 표시될 수 있습니다.  **여기를 클릭하세요.** 를 선택합니다.
    1. 테넌트 전체 정보를 확인하려면 자신에게 필요한 역할을 할당합니다.  **보안 관리자** 를 선택하고 페이지 아래쪽의 **등록** 을 선택합니다.
    1. 루트 관리 그룹이 없다는 메시지가 표시될 가능성이 높습니다.  설명에 따라 시스템에서 그룹을 자동으로 만듭니다.  완료하는 데 최대 15분이 걸리지만 대부분 더 빠르게 완료됩니다.  액세스 권한이 부여되면 페이지의 왼쪽 위 모서리의 ‘권한 얻기’ 위에 있는 **클라우드용 Microsoft Defender** 를 선택합니다. 그런 다음 클라우드용 Microsoft Defender 개요 페이지를 새로 고칩니다.

1. 페이지 위쪽에는 Azure 구독 수, 액세스한 리소스 수, 활성 권장 사항 수, 보안 경고 등의 정보가 표시됩니다.  페이지 주 본문에는 보안 점수, 규정 준수, 인사이트 등을 나타내는 카드가 있습니다.  

1. 페이지 위쪽에서 **액세스한 리소스** 를 선택합니다.  클라우드용 Microsoft Defender 홈페이지 왼쪽 탐색 패널에서 인벤토리를 선택해도 됩니다.
    1. 그러면 **인벤토리** 페이지가 열리고 Azure Pass 구독이 표시됩니다.  **Azure Pass - 스폰서쉽** 을 선택합니다.
    1. 리소스 상태 페이지에서는 권장 사항 목록이 제공됩니다.  제공되는 목록에서 **구독에 둘 이상의 소유자를 할당해야 합니다** 를 선택합니다.
    1. 수정 단계 옆의 드롭다운 화살표를 선택합니다. 세부 수정 단계와 작업 수행을 위한 옵션이 제공됩니다.  
    1. 화면의 왼쪽 위 모서리에서 **클라우드용 Microsoft Defender** 를 선택하여 클라우드용 Microsoft Defender 개요 페이지로 돌아갑니다.

1. 페이지 위쪽에서 **활성 권장 사항** 을 선택합니다.  클라우드용 Microsoft Defender 홈페이지 왼쪽 탐색 패널에서 추천을 선택해도 됩니다.
    1. 권장 사항 페이지에 보안 점수 대시보드가 표시됩니다.
    1. 보안 점수 대시보드 아래에는 컨트롤 목록이 있습니다. 각 보안 컨트롤은 완화해야 하는 보안 위험에 해당됩니다. 해당 컨트롤과 연관된 최대 점수, 현재 점수, 점수를 높일 수 있는 방법, 리소스 상태 관련 정보도 포함되어 있습니다.  
    1. **MFA 사용** 등 컨트롤 중 하나를 선택합니다.  **구독에서 소유자 권한이 있는 계정에 MFA를 사용하도록 설정해야 합니다.** 등 하위 항목 중 하나를 선택합니다.  그러면 열리는 페이지에 설명, 수정 단계, 영향을 받는 리소스가 표시됩니다. 화면 오른쪽 위 모서리에서 **X** 를 선택하여 이 페이지를 종료합니다.
    1. 화면 오른쪽 위 모서리에서 **X** 를 선택하여 권장 사항 페이지를 종료하고 개요 페이지로 돌아옵니다.

1. 주 페이지에서 **규정 준수** 를 선택합니다. 규정 준수 페이지에서는 규정 준수 컨트롤 목록이 제공됩니다.  각 컨트롤 아래에는 평가 집합이 있습니다. 이러한 평가는 Azure에서 클라우드 솔루션을 보호하는 방법에 대한 권장 사항을 제공하는 Azure Security Benchmark를 기준으로 작성된 것입니다.
    1. **IM. ID 관리** 를 선택하고 **IM.6 강력한 인증 컨트롤 사용** 을 선택합니다.  그러면 규정 준수 상태 개선을 위해 고객이 수행할 수 있는 작업 목록이 표시됩니다.
    1. 화면 오른쪽 위에서 **X** 를 선택하여 페이지를 닫고 클라우드용 Microsoft Defender 개요 페이지로 돌아옵니다. 
    1. 다음 작업에서 사용해야 하니 클라우드용 Microsoft Defender 개요 페이지를 계속 열어 두세요.


#### <a name="task-2-in-this-task-you-will-navigate-to-azure-secure-score-and-explore-recommendations-that-can-improve-your-secure-score"></a>작업 2: 이 작업에서는 Azure 보안 점수, 그리고 보안 점수를 높일 수 있는 권장 사항을 살펴봅니다. 

1. 클라우드용 Microsoft Defender 개요 페이지에서 **보안 점수** 카드를 선택합니다.
1. **Azure Pass - 스폰서쉽** 을 선택합니다.  보안 점수를 확인합니다.
1. 권장 사항 페이지에서 **보안 모범 사례 구현** 을 선택하여 목록을 확장합니다. 리소스 상태가 빨간색으로 표시됩니다.
1. 리소스 상태가 빨간색으로 표시되는 **구독에 둘 이상의 소유자를 할당해야 합니다.** 항목을 선택합니다. 
1. **영향받는 리소스** 아래에 비정상 리소스가 선택되거나 밑줄이 표시되어 있는지 확인한 다음, 나열된 Azure 구독을 선택합니다.
1. 액세스 제어(IAM) 페이지 위쪽에서 **+ 추가** 를 선택하고 드롭다운에서 **역할 할당 추가** 를 선택합니다.
    1. 페이지 왼쪽에서 나열된 첫 번째 항목인 **소유자** 를 선택하여 행이 회색으로 강조 표시되게 한 다음, 페이지 아래쪽에 있는 **다음** 을 선택합니다.
    1. 멤버 옆에 있는 **+ 멤버 선택** 을 선택합니다. 
    1. 화면 오른쪽에 열리는 멤버 선택 창에서 **Alex Wilber** 를 선택한 다음 페이지 아래쪽에 있는 **선택** 을 누릅니다.  
    1. 역할 할당 추가 페이지에서 Alex Wilber가 멤버로 나열되었는지 확인하고, **다음** 을 선택한 다음 **검토 + 할당** 을 선택합니다.
    1. 상태가 업데이트되려면 최대 24시간이 걸릴 수 있습니다. 상태가 업데이트되고 나면 액세스 및 권한 관리 그룹의 모든 항목이 요건을 충족하므로, 보안 점수도 업데이트됩니다.
    1. 페이지의 왼쪽 위 모서리의 Azure Pass 위에 있는 **클라우드용 Microsoft Defender** 를 선택하여 클라우드용 Microsoft Defender 개요 페이지로 돌아갑니다.
1. 후속 작업을 위해 이 페이지를 열어 두세요.


#### <a name="task-3--recall-that-microsoft-defender-for-cloud-is-offered-in-two-modes-without-enhanced-security-features-free-and-with-enhanced-security-features-which-are-available-through-the-microsoft-defender-for-cloud-plans-in-this-task-you-discover-how-to-enabledisable-the-various-microsoft-defender-for-cloud-plans"></a>작업 3:  클라우드용 Microsoft Defender는 향상된 보안 기능이 없는 모드(무료)와 클라우드용 Microsoft Defender 요금제를 통해 사용할 수 있는 향상된 보안 기능이 포함된 모드로 제공됩니다. 이 작업에서는 다양한 클라우드용 Microsoft Defender 요금제를 사용하거나 사용하지 않도록 설정하는 방법을 알아봅니다.

1.  클라우드용 Microsoft Defender 개요 페이지의 왼쪽 탐색 패널에서 **환경 설정** 을 선택합니다.
1. 테넌트 루트 그룹 옆에 있는 보다 큼 **>** 기호를 선택하여 확장한 다음(다른 페이지로 이동하므로 테넌트 루트 그룹을 바로 클릭하면 안 됩니다) **Azure Pass - 스폰서쉽** 을 선택합니다.
1.  Defender 요금제 페이지에서 모든 요금제를 활성화하거나 개별 Defender 요금제를 선택하는 방법을 확인합니다. 설정값을 그대로 유지하여 모든 요금제가 해제되게 합니다.
1.  이제 브라우저 탭을 닫아 Azure Portal을 종료해도 됩니다.


#### <a name="review"></a>검토
이 랩에서는 클라우드용 Microsoft Defender를 살펴보고 조직의 보안 태세 개선을 위해 Azure 보안 점수를 사용하는 방법을 알아보았습니다.

