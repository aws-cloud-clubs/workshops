## IAM 보안 주체(Principals), 사용자(Users), 및 정책(Policies)

IAM을 통해 모든 보안 주체(Principals)는 요청을 할 수 있는 권한을 가집니다. _보안 주체_ 란 인증된 후 운영 요청을 할 수 있는 권한이 부여된 사용자, 서비스 또는 계정입니다. 이 규칙의 약간의 예외는 데이터 검색인데, 특정 경우 익명 사용자에게 데이터 접근 권한을 부여하도록 설정할 수 있습니다. 예를 들어, 학교 웹사이트 방문자가 브로셔를 다운로드하려고 할 때, 해당 정보는 공개적으로 공유해도 괜찮기 때문에 신원을 드러내지 않고 다운로드할 수 있습니다. 수천 명의 방문자가 동일한 정보를 요청할 수 있으므로, 이러한 요청을 인증하는 추가적인 오버헤드는 필요하지 않습니다. 그러나 민감한 정보가 익명 사용자에게 노출되지 않도록 데이터를 신중하게 다루어야 합니다.

주요 보안 주체 유형은 다음과 같습니다:

> - 사용자(Users)
> - 역할(Roles)
> - Amazon, Facebook 또는 다른 서드파티 연합 사용자(Federated users)
> - AWS 계정 및 서비스(AWS Accounts & Services)

IAM은 요청에 대해 허용(allow) 또는 거부(deny) 작업으로 응답합니다. 즉, 요청은 권한에 따라 허용되거나 거부됩니다. 사용자가 인증되었다고 해서 반드시 특정 작업을 수행할 권한이 부여된 것은 아닙니다. 다시 체육관 예시를 떠올려 보세요. 시설 내에 학생들이 들어갈 수 없는 직원 사무실이나 전기실과 같은 장소가 있습니다. 마찬가지로 클라우드 리소스에서도 사용자는 가상 컴퓨팅 인스턴스에 접근할 수 있지만, 이를 수정하거나 삭제할 권한은 거부될 수 있습니다.

권한은 주체에게 _IAM 정책(policies)_ 을 통해 부여됩니다. 정책은 경량 데이터 교환 형식 언어인 JSON(JavaScript Object Notation)으로 작성된 명령문입니다.

다음은 IAM 정책의 작동 예시입니다:

[![IAM policy](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/iam-policy-at-work.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/iam-policy-at-work.png)


`student-group`에 할당된 사용자가 보안 주체입니다. 그룹에 연결되거나 첨부된 정책은 학생들에게 웹 포털 리소스를 작업할 수 있는 권한을 부여합니다. 반대로, 학생들에게 학점표 리소스에 대한 권한을 부여하는 정책은 없으므로, 접근이 허용되지 않습니다. 이 예시에서, 권한은 오직 `professor-group`에게만 부여됩니다. 클라우드 환경에서 개발자가 애플리케이션을 빌드하고 테스트할 수는 있지만, 가격 데이터나 제품 재고와 같은 정보에 접근하지 못하게 제한하는 것은 흔한 분리 작업 방식입니다.

IAM 정책에는 두 가지 유형이 있습니다: _주체 기반 정책(identity-based policies)_ 과 _리소스 기반 정책(resource-based policies)_. 주체 기반 정책은 앞서 정의한 주체에 적용되고, 리소스 기반 정책은 AWS 서비스에 적용됩니다.


> 몇 가지 실습에서는 JSON으로 작성된 기본적인 정책 예시를 다룰 것입니다. JSON의 프로그래밍 개념과 기본 구조를 배우는 것은 이번 워크숍의 범위를 벗어납니다. JSON 언어에 대해 더 배우고자 한다면 [JSON 표준](https://www.json.org/json-en.html) 및 [AWS IAM 사용자 가이드](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/introduction.html)를 참고할 수 있습니다.


다음 섹션에서는 사용자와 정책에 대해 더 알아보고, 리소스를 생성하는 몇 가지 실습을 진행하겠습니다.
