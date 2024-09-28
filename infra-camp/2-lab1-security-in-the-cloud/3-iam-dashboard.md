## IAM 대시보드

AWS 관리 콘솔의 IAM 섹션 탐색을 알아봅시다. 워크숍을 위해 AWS 계정에 접근하는 두 가지 방법이 있습니다. 아래에서 귀하의 계정 접근 시나리오에 적합한 탭을 선택하세요. [AWS 계정을 생성하고 활성화하는 방법](https://aws.amazon.com/ko/premiumsupport/knowledge-center/create-and-activate-aws-account/)에 대해 자세히 알아보세요.

### AWS 계정 접근 방법

<details>
  <summary>개인 계정 사용</summary>
  
  AWS 계정에 대한 접근 권한이 있는 경우 (즉, 제공되지 않은 개인 계정을 사용) 이 워크숍 기간 동안 계속해서 진행하십시오. **_중요_:** AWS 서비스를 사용하면 요금이 발생할 수 있습니다. [AWS 요금](https://aws.amazon.com/ko/pricing/)을 참조하여 IAM, VPC, S3와 같은 서비스를 사용할 때 발생할 수 있는 요금에 대해 검토하십시오.
  
</details>

<details>
  <summary>AWS에서 제공한 계정 사용</summary>
  
  강사로부터 워크숍을 완료하기 위한 AWS 계정이 제공됩니다. 이 계정은 제한적이며, 각 실습을 완료하기 위해 필요한 접근만 허용됩니다. 모든 비용은 AWS에서 부담하며, 워크숍이 완료된 후에는 더 이상 이 계정에 접근할 수 없습니다. 아래 지침을 따라 계정에 액세스하세요:
  
  1. [여기](https://portal.aws.training/)를 클릭하여 워크숍 스튜디오 포털에 접근하세요. 강사가 제공한 이벤트 액세스 코드를 코드 필드에 입력하세요.

  2. 올바른 코드를 입력하면 "로그인" 페이지로 이동됩니다. **이메일 일회성 비밀번호 (OTP)** 버튼을 클릭하세요.
  [![IAM Dashboard Account-2](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-otp.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-otp.png)

  3. 이메일 계정을 입력하고 **비밀번호 전송** 버튼을 클릭하세요.
   [![IAM Dashboard Account-3](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-email-account.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-email-account.png)
  
  4. 받은 편지함에 비밀번호가 도착할 때까지 몇 분 정도 기다리세요. **중요:** 스팸 또는 정크 폴더를 확인하여 이메일이 거기에 도착하지 않았는지 확인하세요. 이메일은 `no-reply@us-east-1.otp.signin.aws.training`과 비슷한 주소에서 발송됩니다.
  5. 이메일을 열고 일회성 비밀번호를 복사한 다음, 12자리 값을 비밀번호 필드에 붙여 넣으세요.
  [![IAM Dashboard Account-5](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-passcode-entry.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-passcode-entry.png)

  6. 다음 화면에서 **이용 약관 동의** 박스를 체크하세요.

  7. 왼쪽 화면에서 **AWS 콘솔 열기** 버튼을 클릭하세요. 그러면 새 탭이 열리고 AWS 관리 콘솔로 이동됩니다.
  
  [![IAM Dashboard Account-7](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-mgmt-console.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/sign-in-mgmt-console.png)

  축하합니다! 이제 실습을 위한 준비가 되었습니다!

</details>

계정에 접근한 후:

1. 충분한 관리자 권한이 있는 사용자로 로그인합니다.
   **참고:** 제공된 계정의 경우, 사용자에게 적절한 권한이 부여됩니다.

2. [IAM 대시보드](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)로 이동하여 사용자 계정, 정책 및 기타 IAM 리소스에 대한 정보를 확인합니다.

3. 왼쪽 열의 **액세스 관리**에서 _정책(Policies)_ 을 선택합니다.

4. 정책 필터 검색창에 `AdministratorAccess`를 입력하고 `<Enter>` 키를 눌러 _AdministratorAccess_ 정책을 찾습니다.

5. 정책 이름 옆에 있는 ‘+’ 아이콘을 클릭하여 정책 세부정보를 확장하고 확인합니다.


[![IAM Dashboard1](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-AdministatorAccess-policy-1.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-AdministatorAccess-policy-1.png)


교수들이 새로운 CS 포털을 구축하도록 허락했기 때문에 모든 작업을 수행할 수 있는 충분한 권한이 필요합니다. 위의 설명에서 두 개의 와일드카드 ‘*’ 문자가 있는 점을 주목하세요. 이는 정책이 모든 리소스에서 무제한 작업을 수행할 수 있음을 나타냅니다. 이 수준의 권한이 부여된 사용자는 계정 전반에 걸쳐 작업을 수행할 때 주의해야 합니다.

비교를 위해, 사용자에게 부여할 수 있는 다른 수준의 권한을 살펴보겠습니다.

6. 정책 필터 검색창에서 현재 값을 지우고, 새 검색어로 `AmazonS3ReadOnlyAccess`를 입력합니다. 정책 세부정보를 다시 확장하여 확인합니다.

이 정책과 이전 정책 간의 차이를 주목하세요. 이 정책이 부여된 사용자의 작업은 몇 가지 특정 작업으로 제한됩니다. 이는 사용자가 특정 작업을 수행하는 데 필요한 권한만 부여받는 '_최소 권한의 원칙(principle of least privilege)_' 보안 원칙과 일치합니다.

[![IAM Dashboard2](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-AmazonS3ReadOnlyAccess-v2.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-AmazonS3ReadOnlyAccess-v2.png)