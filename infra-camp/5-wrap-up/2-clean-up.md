# 정리

마지막 단계로 워크숍 전반에 걸쳐 사용된 리소스를 정리해 보겠습니다. 주로 S3 객체와 S3 버킷 제거에 초점을 맞출 것입니다. 이 단계들은 여러분이 개인 AWS 계정을 사용하고 있다면 매우 중요합니다. ***제거되지 않은 객체들은 계속해서 계정에 요금이 부과될 것입니다.***

S3 버킷을 삭제하지 않고 S3 객체만 삭제하는 방법:

1. [S3 dashoard ](https://console.aws.amazon.com/s3)에 로그인합니다.
2. 워크숍 과정에서 생성한 S3 버킷을 클릭합니다.
3. 각 체크박스를 클릭하여 제거할 객체를 선택하세요; 그 다음, *삭제*를 클릭하세요
   ![S3-dashboard-delete-all-objects](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/storage/s3-dashboard-delete-all-objects.png)

**객체 삭제** 화면에서 작업을 확인하기 위해 입력 필드에 `영구 삭제`나 `permanently delete`를 입력한 다음, *객체 삭제*를 클릭하세요. 완료되면 화면 상단에 **객체가 성공적으로 삭제되었습니다** 메시지가 나타날 것입니다. 더 이상 필요하지 않은 다른 버킷의 객체들도 동일한 단계를 수행하여 삭제하세요.

S3 버킷과 그 안에 저장된 모든 객체를 삭제하려면:

1. [S3 dashoard ](https://console.aws.amazon.com/s3) 에 로그인하세요.
2. 제거할 S3 버킷의 라디오 버튼을 선택하고, 오른쪽 상단의 *비우기* 버튼을 클릭하세요.

빈 버킷이 된 화면에서,  입력란에 `영구 삭제`나 `permanently delete`를 입력하여 작업을 완료한 다음 *비우기*를 클릭하세요.

![S3-dashboard-delete-all-objects](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/storage/s3-dashboard-delete-bucket.png)

S3 버킷이 삭제되었는지 확인하세요.