VPC 생성
=

개념을 시연하고 성가신 프랑스 학생들이 우리 시스템에 들어가지 못하도록 VPC를 만들어봅시다!

---

1. AWS 계정에 로그인합니다.

2. VPC 서비스 대시보드로 이동합니다. - https://console.aws.amazon.com/vpc/
   ![image](https://github.com/user-attachments/assets/aa2932f6-7b1d-4653-b108-b6bc56f2c699)

3. 대시보드에서 *VPC 생성*을 선택합니다.

4. **생성할 리소스**에서 VPC만 선택합니다.

5. **이름 태그 - _선택 사항_**. VPC의 이름을 입력하세요.
   - 이 단계는 선택 사항이지만 이렇게 한다면 나중에 VPC를 더 쉽게 식별할 수 있는 키:값 쌍이 생성됩니다. VPC에 `cs-dep-vpc` 라는 이름을 입력하세요.

6. **IPv4 CIDR 블록**의 경우, *IPv4 CIDR 수동 입력*을 선택하고 VPC의 IPv4 주소 범위를 입력합니다 ('IPAM 할당 IPv4 CIDR 블록'을 선택하지 마세요).

7. IPv4 CIDR 필드에 유효한 IP 주소 범위(예: `10.32.0.0/16`)를 입력하세요. 이 필드를 비워두지 마세요.
   ![image](https://github.com/user-attachments/assets/1168bf8a-b9ac-4765-a485-e11eddd522f0)

8. 다음 두 필드의 **IPv6 CIDR 블록**과 **테넌시**를 기본값으로 설정합니다.

9. VPC에 태그를 추가하려면 **태그 추가**를 클릭하고 "key:value" 쌍을 입력합니다. **_참고_**: 이 단계는 선택 사항이며 첫 번째 태그는 이미 생성되었습니다.

10. **VPC 생성**을 클릭합니다.

![image](https://github.com/user-attachments/assets/ef6ce411-714f-43fc-b2ea-018ba3fc0b19)

이게 다예요... 클라우드 데이터 센터가 이제 막 만들어졌어요!
