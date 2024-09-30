VPC 서브넷
=

우리가 방금 만든 VPC에 대해 두 개의 서브넷을 추가합시다.
*서브넷*은 VPC 내부에 정의된 IP 주소 범위입니다.
서브넷은 인터넷 연결을 허용하는 "공개"로 구성하거나 인터넷 연결이 허용되지 않는 "비공개"로 구성할 수 있습니다.

여기서는 퍼블릭 및 프라이빗 서브넷 모두에 대한 주소 범위를 생성합니다.

1. VPC 서비스 대시보드로 이동합니다. - https://console.aws.amazon.com/vpc/

2. 왼쪽 사이드바의 _서브넷_ 메뉴를 클릭한 다음 _서브넷 생성_ 버튼을 클릭합니다. **_참고_**: 사용 가능한 다른 서브넷이 표시될 수도 있습니다. 이 연습에서는 무시해도 됩니다.
   ![image](https://github.com/user-attachments/assets/41ad58ef-681f-4d5b-b0a6-7665a53265b5)

3. **VPC ID**의 경우 방금 만든 VPC를 선택합니다.
   ![image](https://github.com/user-attachments/assets/0975b518-00b2-4197-ba61-d809b5071d04)

4. **서브넷 설정** 섹션에서 아래와 같이 이름과 IP 범위 값을 입력하여 `public-subnet` 및 `private-subnet` 서브넷을 생성합니다.
   ![image](https://github.com/user-attachments/assets/6d5ac6a1-0f47-4598-82cc-8148c4415c48)<br><br>
   **_참고_**: 두 번째 서브넷을 생성하려면 *새 서브넷 추가 버튼*을 클릭합니다.<br>
   ![image](https://github.com/user-attachments/assets/44946479-87ba-44d7-b1fe-cd827dec7f1f)<br>
   ![image](https://github.com/user-attachments/assets/2e36be1a-f4ee-47d7-adc6-04bf36faae70)

6. 다음으로, _서브넷 생성_ 버튼을 클릭합니다.

7. *public-subnet*과 _private-subnet_ 리소스가 생성되었는지 확인합니다.

현재 퍼블릭 서브넷은 이름으로 표시된 대로 *퍼블릭*입니다.<br>
인터넷에서 리소스에 접근하려면 몇 가지 추가 단계를 수행해야 합니다.<br>
이러한 단계에는 인터넷 게이트웨이 리소스 및 라우팅 테이블 생성이 포함됩니다.<br>
일반적으로 이러한 단계는 이 워크숍의 범위를 벗어나는 것으로 간주하므로 Amazon VPC 사용 설명서를 참조하시기 바랍니다.<br>- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-example-dev-test.html <br>
하지만 학과의 자원을 보호해야 하는 CS 관리자들이니, 우리는 이 작업을 확실하게 해낼 것입니다!<br>
다음 과제의 일환으로 이러한 단계를 처리해 보겠습니다.
