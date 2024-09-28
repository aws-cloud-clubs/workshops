[원문 사이트](https://catalog.us-east-1.prod.workshops.aws/workshops/781f1e70-d6e9-4f0d-8c7e-b069990a4f8c/en-US/introduction)

# 소개

클라우드에서 애플리케이션 개발을 위한 첫 걸음을 내딛는 것은 부담스러울 수 있습니다. cloud-native 방식에 적응하는 것은 어느정도의 시간이 필요한데요. 특히 시스템 개발에 익숙하지 않거나 이전의 on-premise 방식의 리소스 관리에 익숙한 경우에는 더욱 그렇습니다. 이 워크샵을 통해 여러분은 AWS 서비스와 개념에 익숙해지면서, 클라우드에 대한 지식과 자신감을 키울 수 있을 것입니다.

이 워크샵은 약 90분 동안 진행되며, AWS 서비스를 소개하고 핵심 용어를 설명한 후, 실제로 AWS 클라우드 리소스를 구축하는 과정을 함께합니다.



> ℹ️ **시작하기 전에 간단한 퀴즈로 여러분의 지식을 테스트해봐요!**
>
> ### **워크샵 사전 퀴즈**
>
> 각 질문을 읽고 정답을 고르세요. 질문을 이해하지 못하거나 답이 확실하지 않더라도 괜찮습니다. 각 질문에 대한 답을 검토하는 데 몇 분 정도 시간을 할애할 것입니다.
>
> 1. *"구성 요소 간의 상호 의존성을 줄여 실패와 중단을 최소화하는"* 애플리케이션 설계 접근 방식을 무엇이라고 하는가?
>
>    a) 협업(Collaboration)
>
>    b) 집합(Aggregation)
>
>    c) 분리(Decoupling)
>
>    d) 이전(Migration)
>
> 2. *"특정 작업을 수행하는 데 필요한 요구사항에만 기반하여 사용자 권한을 부여하는"* 관리자들은 어떤 보안 개념을 구현하고 있는가?
>
>    a) 전송 중 데이터 암호화(Data Encryption in transit)
>
>    b) 최소 권한의 원칙(Principle of least privilege)
>
>    c) 사용자 활동의 '누가, 무엇을, 언제, 어디서'(The *'who, what, when, and where'* of user activity)
>
>    d) 침투 테스팅(Penetration testing)
>
> 3. 서비스 제공업체는 [       ]에 대한 책임이 있고, 고객은 [       ]에 대한 책임이 있다.
>
>    a) 클라우드 "자체"의 보안(security "of" the cloud); 클라우드 "내부"의 보안(security "in" the cloud)
>
>    b) 건물의 물리적 보안(physical security of buildings); 데이터와 애플리케이션에 대한 접근 권한(access permissions to data and applications)
>
>    c) 전력, 냉각, 유지보수(power, cooling, and maintenance); 계정 접근, 결제 관리(account access, billing management)
>
>    d) 위의 모든 사항(all of the above)
>
> 4. 'API'라는 용어는 무엇의 약자인가?
>
>    a) Application Programming Interconnect
>
>    b) Algorithm Prediction Intelligence
>
>    c) Application Programming Interface
>
>    d) Advanced Programming Interface

어떠셨나요? 다시 한번 말씀드리지만, 여러분이 이 워크숍을 마칠 때쯤이면 이런 질문들과 그 외 많은 것들이 명확해질 거예요. **시작해봅시다!**
