<a name="---"></a><!---
---
데모: 제목: ‘Azure Policy’ 학습 경로/모듈/단원: ‘학습 경로: Microsoft 규정 준수의 기능 설명, 모듈 6: Azure의 리소스 거버넌스 기능에 대해 설명, 단원 2: Azure Policy 설명’
---
--->

# <a name="demo-azure-policy"></a>데모: Azure Policy

이 데모는 다음 Learn 콘텐츠에 매핑됩니다.

- 학습 경로: Microsoft 규정 준수의 기능 설명
- 모듈: Azure의 리소스 거버넌스 기능 설명
- 단원: Azure Policy 설명

## <a name="demo-scenario"></a>데모 시나리오

이 데모에서는 Azure 정책을 설정하는 프로세스를 단계별로 진행하고 해당 정책 적용 시의 영향을 살펴봅니다.

### <a name="demo-part-1"></a>데모 1부

리소스 그룹에 태그를 지정해야 하는 정책을 만듭니다(템플릿에서 정책을 만드는 단계 진행).

1. Microsoft Edge를 엽니다. 주소 표시줄에 **portal.azure.com**을 입력합니다.  로그인되어 있지 않다면 관리자 자격 증명을 사용하여 로그인합니다.

1. 검색 상자(페이지 위쪽의 'Microsoft Azure' 옆에 있는 파란 막대)에 **policy**를 입력하고 검색 결과에서 **Policy**를 선택합니다.

1. 그러면 정책 페이지의 개요가 표시됩니다. 대시보드에서 제공되는 정보를 살펴봅니다.

1. 왼쪽 탐색 패널의 작성 아래에서 **할당**을 선택합니다.  정책 할당 항목이 이미 있습니다. **ASC 기본값**을 선택합니다.  설명 필드를 검토합니다. 참고: 설명 필드는 클라우드용 Microsoft Defender로 리브랜딩된 Azure Security Center를 참조합니다.  페이지 오른쪽 위 모서리에서 **X**를 선택하여 정책 할당 페이지로 돌아옵니다.

1. 페이지 위쪽에서 **정책 할당**을 선택합니다. 관리자에게 정책 할당 프로세스를 안내하는 정책 할당 마법사가 열립니다.

1. 기본 탭에서 시작합니다.
    1. 범위의 경우 기본 설정을 그대로 둡니다. 이 경우 정책의 범위는 ALH(권한 있는 랩 호스터)에서 제공하는 Azure 구독입니다.
    1. 정책 정의에서 **줄임표**를 선택합니다.  사용 가능한 정책 정의 목록이 제공됩니다.  검색 창에 **태그 필요**를 입력합니다. 검색 결과에서 **리소스 그룹에 태그 필요**를 선택하고(아래쪽으로 스크롤해야 할 수 있음) **선택**을 누릅니다.  참고: 이 정책을 적용하면 요구 사항을 충족하지 않는 새 리소스 그룹 만들기가 거부됩니다.  
    1. 기본 할당 이름을 확인합니다.  이름을 그대로 유지합니다.
    1. 정책 적용이 **사용**으로 설정되어 있는지 확인하고 **다음**을 선택합니다.

1. 이제 매개 변수 탭에 있습니다. 태그 이름 필드에 **환경**을 입력하고 **다음**을 선택합니다.

1. 수정 탭에서 기본 설정을 그대로 두고 **다음**을 선택합니다.

1. 이제 비준수 메시지 탭에 있습니다. 비준수 메시지 필드에 **환경 태그가 필요합니다**를 입력하고 **다음**을 선택합니다. 참고: 정책 할당 전에 만들었으며 환경 태그가 지정되어 있지 않은 리소스 그룹에 비준수 이유로 이 메시지가 표시됩니다.  

1. 정책 할당을 검토한 다음 **만들기**를 선택합니다.  정책이 바로 표시되지 않으면 **새로 고침**을 선택합니다. 참고: 정책이 적용되는 데 최대 30분이 걸릴 수 있지만 일반적으로는 훨씬 더 빨리 적용됩니다.

1. 화면 오른쪽 위 모서리에서 **X**를 선택하여 정책 할당 페이지를 종료합니다.

1. 그러면 Azure 서비스 홈페이지가 표시됩니다.  다음 작업에 필요합니다. 이 페이지를 열어 두세요.

### <a name="demo-part-2"></a>데모 2부

이 작업에서는 태그가 없는 Azure에 리소스 그룹을 만들려고 시도하여 Azure 정책 할당의 영향을 확인할 수 있습니다.

1. 브라우저 탭에서 홈 - Microsoft Azure를 엽니다.

1. 페이지 위쪽의 Azure 서비스 아래에서 **리소스 그룹**을 선택합니다.

1. 페이지 왼쪽 위 모서리에서 **+ 만들기**를 선택합니다.

1. 리소스 그룹 만들기의 기본 탭에서 구독 필드를 현재 값으로 유지합니다.

1. 리소스 그룹 필드에 **SC900-Labs**를 입력합니다.

1. 지역 설정은 기본값으로 유지하고 **다음: 태그**를 선택합니다.

1. 태그 이름과 값 필드는 비워 둡니다.  해당 필드에 내용을 입력하지 마세요. 다음으로 **검토 + 만들기**를 선택합니다.

1. 유효성 검사에 통과했다는 메시지가 표시되면(태그 이름과 값은 마법사에서 필수 필드가 아님) **만들기**를 선택합니다.

1. 화면 맨 위에 다음과 같은 오류 메시지가 표시됩니다. “리소스 그룹을 만들지 못했습니다. **오류 세부 정보 보기**를 선택합니다.” Azure 정책에 포함된 조건이 충족되지 않았으므로 비준수 사항으로 인해 리소스 그룹 만들기가 거부되었습니다. 참고: 오류 메시지가 표시되지 않고 리소스 그룹이 만들어졌다면 정책이 아직 적용되지 않았기 때문입니다.  이전 작업에서 만든 정책의 정책 페이지로 이동합니다. 정책이 적용되면 해당 리소스가 규정을 준수하지 않음이 표시됩니다.  그리고 세부 정보 페이지에 비준수 메시지가 표시됩니다.

1. 오류 요약에는 오류 유형으로 "정책에서 'SC900-Labs' 리소스를 허용하지 않았습니다."가 표시됩니다.  화면 왼쪽 위 모서리에서 **X**를 선택하여 이 창을 닫습니다.

1. 리소스 그룹 만들기 창에서 **이전**을 선택합니다.

1. 리소스 그룹 만들기의 태그 페이지가 다시 표시됩니다.  이름 필드에 환경을 입력하고 값 필드에 **SC900-Labs**를 입력한 후에 **다음: 검토 + 만들기 >** 를 선택합니다.

1. 태그를 확인하고 **만들기**를 선택합니다.

1. 이름 필드에 **환경**을 입력하고 값 필드에 **Labs**를 입력한 다음(이 값은 무엇이든 될 수 있으며 정책에는 태그 값만 필요), **다음: 검토 + >만들기 >** 를 선택하고 **만들기**를 선택합니다.

1. 리소스 그룹이 나열됩니다.  

1. 정책 이전에 만든 리소스 그룹이 있으면 해당 리소스 그룹은 이 정책 할당에 대해 비준수로 표시되며 이는 환경 태그를 적용하여 수정해야 한다고 학습자에게 알립니다.  ResourceGroup1이라는 레이블로 지정된 기존 리소스 그룹이 비준수로 표시되어 수정이 필요한 상태이지만 수정을 한 후 상태가 업데이트되는 시간은 랩 환경에서의 일반적인 시간 보다 길어집니다.

### <a name="review"></a>검토

이 데모에서는 Azure 정책을 설정하는 프로세스와 해당 정책 적용 시의 영향을 살펴보았습니다.
