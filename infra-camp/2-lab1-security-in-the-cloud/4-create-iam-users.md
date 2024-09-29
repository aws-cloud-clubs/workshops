## IAM Users 생성

우리가 방금 배운 지식을 활용하여 몇 가지 리소스를 생성해 보겠습니다. 먼저 IAM 그룹을 생성한 다음, 해당 그룹에 추가할 두 개의 IAM 사용자를 생성하겠습니다. _그룹_ 은 IAM 사용자들의 모음으로, 동시에 권한 관리를 적용할 수 있습니다.

1. [IAM 콘솔](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/home)로 이동합니다.

2. **User Group(사용자 그룹) > Create Group(그룹 만들기)** 를 클릭하여 AWS 사용자 그룹을 생성합니다. 그룹 이름을 `PowerUserGroup`으로 설정합니다.

3. 현재는 _Add users(사용자 추가)_ 옵션을 건너뜁니다.

4. **Attach permissions policies(권한 정책 연결)** 아래에서 `PowerUserAccess` 정책을 검색합니다.

5. 정책 옆의 체크박스를 선택하여 그룹에 연결한 후, 페이지 하단의 _Create Group(그룹 만들기)_ 를 클릭합니다.

[![IAM Users-1](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-group-1.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-group-1.png)

[![IAM Users-2](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-group-2.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-group-2.png)


이제 IAM 그룹에 권한 정책이 연결되었습니다. 그룹에 추가된 모든 사용자는 연결된 정책의 권한을 상속받게 됩니다.

1. 페이지 왼쪽에서 **사용자(Users)** 를 클릭한 다음, _Add users(사용자 추가)_ 를 클릭합니다.

2. 사용자 이름을 `student-user1`로 입력합니다. _Provide user access to the AWS Management Console(AWS 관리 콘솔에 사용자 접근 권한 제공)_ 옵션을 체크합니다.

3. 다음 섹션에서 _IAM 사용자 생성(I want to create an IAM user)_ 을 선택합니다.

4. _사용자 지정 비밀번호(Custom password)_ 를 선택하고, 유효한 비밀번호를 입력합니다. 비밀번호는 문자 제한 및 문자 유형을 만족해야 합니다. 
   **중요**: 나중에 이 사용자 ID로 로그인해야 할 경우를 대비하여 생성한 비밀번호를 기록해 두십시오.

5. _사용자는 다음 로그인 시 새 비밀번호를 생성해야 합니다(권장)_  옵션을 체크 해제합니다. 이를 통해 로그인 시 비밀번호를 다시 생성하지 않아도 됩니다.
페이지 하단의 _다음(Next)_ 버튼을 클릭합니다.

[![IAM Users-3](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-pt1a.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-create-new-user-pt1a.png)

6. **권한 설정(Set permissions)** 페이지에서:

a) _사용자를 그룹에 추가(Add user to grouop)_ 를 클릭합니다.  
b) _사용자 그룹_ 에서 이전에 생성한 _PowerUserGroup_ 을 선택합니다.  
c) **권한 경계(Permissions boundary)** 섹션은 건너뛰고, **다음**을 클릭합니다.

[![IAM Users-4](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-add-user-to-group-1.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-add-user-to-group-1.png)

7. 검토 및 생성 페이지에서 사용자 정보를 확인한 후, **사용자 생성(Create User)** 을 클릭합니다.

[![IAM Users-5](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-add-user-to-group-2.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-add-user-to-group-2.png)

IAM 사용자가 이제 생성되었습니다. 사용자의 비밀번호가 포함된 `.csv` 파일을 다운로드하는 것은 선택 사항이며, 이전에 비밀번호 정보를 기록했다면 필수는 아닙니다.

_사용자 목록으로 돌아가기(Return to users)_ 버튼을 클릭합니다.

8. 위의 단계를 반복하여 두 번째 사용자 `student-user2`를 생성합니다.

[![IAM Users-6](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-two-users-in-group.png)](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/IAM-dashboard-two-users-in-group.png)


**축하합니다! 두 명의 IAM 사용자를 생성하고, 그들을 IAM 사용자 그룹에 할당했습니다!**
