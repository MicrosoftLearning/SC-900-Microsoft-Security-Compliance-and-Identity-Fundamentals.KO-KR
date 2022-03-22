---
lab:
  title: 코어 eDiscovery 워크플로 살펴보기
  module: 'Module 4 Lesson 4: Describe the capabilities of Microsoft compliance solutions: Describe the eDiscovery and audit capabilities of Microsoft 365'
ms.openlocfilehash: cb7b0e4c2d7b2ac980e829f24ebbdbb31965e2b8
ms.sourcegitcommit: 965f24bd5f74be6d0841bf526259a5651af4fdf5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/02/2022
ms.locfileid: "139253910"
---
# <a name="lab-explore-the-core-ediscovery-workflow"></a>랩: 코어 eDiscovery 워크플로 살펴보기

## <a name="lab-scenario"></a>랩 시나리오
이 랩에서는 코어 eDiscovery를 설정하려면 수행해야 하는 단계를 살펴봅니다. 그런 후에 코어 eDiscovery 워크플로를 진행하면서 eDiscovery 보류 만들기, 검색 쿼리 만들기, 검색 결과 내보내기 작업을 수행합니다.  참고:  코어 eDiscovery 라이선스를 적용하려면 적절한 조직 구독과 사용자별 라이선스가 필요합니다. 코어 eDiscovery를 지원하는 라이선스를 모르는 경우에는 코어 eDiscovery 시작을 방문하세요.


**예상 소요 시간:** 20~25분

#### <a name="task-1--to-access-core-ediscovery-or-be-added-as-a-member-of-a-core-ediscovery-case-a-user-must-be-assigned-the-appropriate-permissions-in-this-task-you-as-the-global-admin-will-add-specific-users-as-members-of-the-ediscovery-manager-role-group"></a>작업 1:  코어 eDiscovery에 액세스하거나 코어 eDiscovery 사례의 멤버로 추가되려면 사용자에게 적절한 권한이 할당되어야 합니다. 이 작업에서는 전역 관리자로 로그인하여 eDiscovery 매니저 역할 그룹의 구성원으로 특정 사용자를 추가합니다.

 Microsoft Edge를 엽니다. 주소 표시줄에 **admin.microsoft.com** 을 입력합니다.

1. 관리자 자격 증명으로 로그인합니다.
    1. 로그인 창에 **admin@WWLxZZZZZZ.onmicrosoft.com** 을 입력하고(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID) **다음** 을 선택합니다.
    
    1. 랩 호스팅 공급자가 제공한 관리자 암호를 입력합니다. **로그인** 을 선택합니다.
    1. 로그인 상태를 유지할지 묻는 메시지가 표시되면 **예** 를 선택합니다. 그러면 Microsoft 365 관리 센터 페이지로 이동됩니다.

1. Microsoft 365 관리 센터의 왼쪽 탐색 창에서 **모두 표시** 를 선택합니다.

1. 관리 센터 아래에서 규정 준수를 선택합니다.  새 브라우저 페이지가 열리고 Microsoft 365 규정 준수 센터 시작 페이지가 표시됩니다.  

1. 왼쪽 탐색 창에서 **권한** 을 선택합니다. 

1. 권한 및 역할 페이지의 규정 준수 센터에서 **역할** 을 선택합니다.

1. 검색 창에 **eDiscovery** 를 입력하고 검색 아이콘(돋보기)을 선택합니다.  **eDiscovery 매니저** 를 선택합니다.

1. 그러면 열리는 창에서 2개 하위 그룹인 eDiscovery 매니저 및 eDiscovery 관리자를 확인합니다.  각 그룹의 설명을 확인합니다.  이 랩에서는 eDiscovery 관리자 하위 그룹에 구성원을 추가합니다. eDiscovery 관리자 옆에 있는 **편집** 을 선택합니다.  일반 모범 사례에 따라 사용자에게는 해당 역할에 필요한 최소 권한을 할당해야 합니다.

1. 이 역할 그룹에 구성원을 추가하려면 **eDiscovery 관리자 선택** 탭이 표시되어 있는지 확인하고 **eDiscovery 관리자 선택** 을 선택합니다.

1. 페이지 위쪽에서 **+ 추가** 를 선택합니다.

1. 이름 목록에서 MOD 관리자, Megan Bowen을 선택하고 페이지 아래쪽에서 추가를 선택합니다. 그런 후에 페이지 아래쪽에서 완료를 선택합니다.   

1. 추가된 구성원이 정확한지 확인하고 **저장** 을 선택합니다.

1. eDiscovery 창 아래쪽에서 **닫기** 를 선택합니다.

1. 다음 작업에서 사용할 것이므로 이 브라우저 탭을 열어 두세요.

#### <a name="task-2--in-this-task-you-as-an-ediscovery-administrator-mod-admin-is-an-ediscovery-administrator-will-create-a-case-to-start-using-core-ediscovery"></a>작업 2:  이 작업에서는 eDiscovery 관리자(MOD 관리자)로 로그인하여 코어 eDiscovery 사용을 시작하기 위한 케이스를 작성합니다.

1. 아직 규정 준수 센터 역할 페이지가 표시되어 있을 것입니다. 이전 작업에서 브라우저 탭을 닫았다면 새 브라우저 탭을 열고 **compliance.microsoft.com** 을 입력합니다.

1. 왼쪽 탐색 패널의 솔루션 아래에서 **eDiscovery** 를 선택하고 **코어** 를 선택합니다.

1. 코어 eDiscovery 페이지 위쪽에서 **+ 케이스 만들기** 를 선택합니다.

1. 새 케이스 창에 케이스 이름 **SC900 Test Case** 를 입력하고 페이지 아래쪽에서 **저장** 을 선택합니다.

1. 이제 목록에 케이스가 표시됩니다.

1. 사용자가 케이스 작성자이며 eDiscovery 관리자 권한을 소유하고 있으므로 해당 케이스 관련 작업을 시작할 수 있습니다.  

1. 후속 작업에서 사용할 것이므로 이 브라우저 탭을 열어 두세요.

#### <a name="task-3--now-that-you-have-created-a-core-ediscovery-case-you-can-begin-to-work-with-the-case--in-this-task-you-will-create-an-ediscovery-hold-for-the-case-for-you-just-created--specifically-you-will-crate-a-hold-for-the-the-exchange-mailbox-belonging-to-adele-vance"></a>작업 3:  이제 코어 eDiscovery 케이스를 만들었으므로 해당 케이스 관련 작업을 시작할 수 있습니다.  이 작업에서는 방금 만든 케이스에 대해 eDiscovery 보류를 작성합니다.  구체적으로는 Adele Vance 소유의 Exchange 사서함을 대상으로 보류를 작성합니다.

1. 브라우저에서 코어 eDiscovery 탭을 엽니다.

1. 코어 eDiscovery 페이지에서 이전 탭에서 만든 케이스인 **SC900 Test Case** 를 선택합니다. 

1. 케이스의 홈 페이지에서 **보류** 탭을 선택한 다음 **+만들기** 를 선택합니다.

1. 이름 필드에 **Test hold** 를 입력하고 다음을 선택합니다.

1. 위치 선택 페이지에서 **Exchange 사서함** 옆의 토글 스위치를 선택하여 상태를 **켜기** 로 설정하고 **사용자, 그룹 또는 팀** 을 선택합니다.  검색 상자에 Adele을 입력하고 키보드의 Enter 키를 누릅니다. 검색 결과에서 **Adele Vance** 를 선택하고 선택, **완료** 를 차례로 선택합니다.

1. 위치 선택 페이지에서 **다음** 을 선택합니다.  여기서는 랩을 빠르게 진행하기 위해 이 보류에 다른 위치를 포함하지 않습니다.

1. 쿼리 조건 페이지에서는 충족되는 조건이나 특정 키워드를 기준으로 보류를 만들 수 있습니다. **+조건** 을 선택하여 사용 가능한 옵션을 확인합니다.  **다음** 을 선택합니다. 조건이 없으면 보류에서 지정된 위치에 모든 콘텐츠가 보존됩니다.

1. 설정을 검토하고 **제출** 을 선택합니다. 제출은 몇 분 정도 걸릴 수 있습니다. 제출이 완료되면 완료를 선택합니다.  목록에 Test hold가 표시됩니다.  해당 검색이 바로 표시되지 않으면 **새로 고침** 을 선택합니다.

1. 후속 작업에서 사용할 것이므로 이 브라우저 탭을 열어 두세요.

#### <a name="task-4--with-a-hold-in-place-you-will-create-a-search-query--once-your-search-is-complete-you-will-go-export-and-download-the-results-for-future-investigation---note--searches-associated-with-a-core-ediscovery-case-are-not-listed-on-the-content-search-page-in-the-microsoft-365-compliance-center-these-searches-are-listed-only-on-the-searches-page-of-the-associated-core-ediscovery-case"></a>작업 4:  보류를 만들었으므로 이번에는 검색 쿼리를 만듭니다.  검색이 완료되면 추가 조사를 위해 결과를 다운로드하여 내보냅니다.   참고:  코어 eDiscovery 케이스와 연관된 검색은 Microsoft 365 규정 준수 센터의 콘텐츠 검색 페이지에 표시되지 않습니다. 이러한 검색은 관련 코어 eDiscovery 케이스의 검색 페이지에만 표시됩니다.

1. 브라우저에서 SC900 Test 케이스 탭을 엽니다.

1. 케이스의 보류 페이지에서 **검색** 을 선택합니다.

1. 검색 페이지에서 **+ 새 검색** 을 선택합니다.

1. 이름 필드에 **Test Hold - Sales Search** 를 입력하고 페이지 아래쪽에서 **다음** 을 선택합니다.

1. 랩 환경에 온-프레미스 사용자가 없으므로 위치 선택 페이지에서 **보류 중인 위치** 를 선택하고 **온-프레미스 사용자에 대한 앱 콘텐츠 추가** 를 선택 취소한 후 **다음** 을 선택합니다.

1. 쿼리 조건 페이지에서는 충족되는 조건이나 특정 키워드를 기준으로 보류를 만들 수 있습니다. 키워드 필드에 **Sales** 를 입력하고 **다음** 을 선택합니다.

1. 설정을 검토하고 **제출** 을 선택합니다. 제출은 몇 분 정도 걸릴 수 있습니다. 제출이 완료되면 완료를 선택합니다.  목록에 검색이 표시됩니다.  해당 검색이 바로 표시되지 않으면 **새로 고침** 을 선택합니다.

1. 검색 창에서 방금 만든 검색인 **Test Hold - Sales Search** 를 선택합니다.  요약 탭이 선택된 창이 열립니다.  검색이 완료되면 검색이 완료되었음을 나타내는 상태가 표시됩니다.  그리고 검색 통계 탭이 표시됩니다(검색 통계 탭이 표시되지 않으면 검색이 아직 실행 중이며 완료되려면 몇 분 정도 걸리는 것일 수 있음).  **검색 통계** 탭을 선택하고 검색 콘텐츠 옆의 드롭다운을 선택합니다.  조건 보고서 및 주요 위치 관련 추가 정보도 확인할 수 있습니다.  

1. 페이지 아래쪽에서 **작업** 을 선택합니다.  사용 가능한 옵션을 확인하고 **결과 내보내기** 를 선택합니다.
    
    1. 결과 내보내기 창에서 기본값을 그대로 유지하고 페이지 아래쪽의 **내보내기** 를 선택합니다. 그러면 자동으로 "Test Hold - Sales Search" 창으로 돌아옵니다. 페이지 아래쪽의 **닫기** 를 선택합니다.
    
    1. SC900-Test 케이스 페이지의 위쪽에서 **내보내기** 를 선택합니다.
    1. **Test Hold - Sales Search_Export** 를 선택합니다.
    1. 그러면 열리는 "Test Hold - Sales Search_Export" 창에 내보내기 키가 표시됩니다. **클립보드에 복사** 를 선택합니다.
    1. 창 위쪽에서 **결과 다운로드** 를 선택합니다. 새 브라우저 페이지가 열리고 이 파일을 열지를 묻는 팝업 창이 표시됩니다. **열기** 를 선택합니다.
    1. 콘텐츠 검색을 처음 다운로드하는 경우 Microsoft Office 365 eDiscovery 내보내기 도구를 설치하라는 메시지가 표시됩니다.  **설치** 를 선택합니다.
    1. 설치가 완료되면 eDiscovery 내보내기 도구 창이 열립니다.  클립보드에 복사했던 내보내기 키를 첫 번째 필드에 붙여넣습니다(키보드에서 Ctrl+V를 누르거나, 마우스 오른쪽 단추를 클릭한 후 붙여넣기 선택).
    1. 두 번째 필드에서는 내보내기 파일을 저장할 위치를 선택하고 **시작** 을 선택합니다.  다운로드 프로세스가 완료되면 **닫기** 를 선택하여 이 브라우저 탭을 닫습니다.
    1. 그러면 "Test Hold - Sales Search_Export" 창이 다시 표시됩니다.  **닫기** 를 선택합니다.
    1. 다운로드 위치로 이동하여 다운로드가 정상적으로 완료되었는지 확인합니다. 


#### <a name="review"></a>검토

이 랩에서는 코어 eDiscovery 사용을 시작하려면 수행해야 하는 단계를 진행했습니다. 구체적으로는 eDiscovery용 역할 권한 설정과 eDiscovery 케이스 만들기를 수행했습니다.  케이스를 만든 후에는 코어 eDiscovery 워크플로를 진행하면서 eDiscovery 보류 만들기, 검색 쿼리 만들기, 추가 조사에 사용하기 위한 검색 결과 내보내기 작업을 수행했습니다.