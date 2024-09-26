[원문 사이트](https://catalog.us-east-1.prod.workshops.aws/workshops/781f1e70-d6e9-4f0d-8c7e-b069990a4f8c/en-US/introduction)

# 소개

클라우드에서 애플리케이션 개발을 위한 첫 걸음을 내딛는 것은 부담스러울 수 있습니다. cloud-native 방식에 적응하는 것은 어느정도의 시간이 필요한데요. 특히 시스템 개발에 익숙하지 않거나 이전의 on-premise 방식의 리소스 관리에 익숙한 경우에는 더욱 그렇습니다. 이 워크샵을 통해 여러분은 AWS 서비스와 개념에 익숙해지면서, 클라우드에 대한 지식과 자신감을 키울 수 있을 것입니다.

이 워크샵은 약 90분 동안 진행되며, AWS 서비스를 소개하고 핵심 용어를 설명한 후, 실제로 AWS 클라우드 리소스를 구축하는 과정을 함께합니다.



> ℹ️ **시작하기 전에 간단한 퀴즈로 여러분의 지식을 테스트해봐요!**
>
> **워크샵 사전 퀴즈**
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



## 학습 목표

이 워크숍을 마쳤을 때, 여러분은 다음과 같은 능력을 갖추게 될 것입니다.

1. AWS에서 애플리케이션을 구축하고 운영하는 데 있어 기반 인프라가 수행하는 역할을 설명할 수 있습니다.
2. *identity management* 의 개념을 이해하고, 다양한 수준의 접근 권한을 가진 사용자를 생성할 수 있습니다.
3. 클라우드 환경에서 리소스를 배포하기 위해 격리된 논리적 네트워크 경계를 구축할 수 있습니다.
4. 클라우드에서 데이터 객체를 저장, 검색하고 보안적으로 안전하게 할 수 있습니다.

이번 워크숍에서는 아래의 세 가지 핵심 서비스를 소개할 것입니다.

- **AWS Identity and Access Management** (AWS IAM) — [https://aws.amazon.com/iam/ ](https://aws.amazon.com/iam/)
- **Amazon Virtual Private Cloud** (Amazon VPC) — [https://aws.amazon.com/vpc/ ](https://aws.amazon.com/vpc/)
- **Amazon Simple Storage Service** (Amazon S3) — [https://aws.amazon.com/s3/ ](https://aws.amazon.com/s3/)

이 서비스들에 대해 잘 모르거나 AWS에 대한 지식이 부족해도 걱정하지 마세요. Hands-on 과정과 더불어, 워크숍 전반에 걸쳐 충분한 정보와 참고 자료가 제공될 예정입니다.



## 사전 준비사항 - 시작하기 위해 필요한 것

이 워크숍을 진행하기 위해, 참여자는 다음이 필요합니다.

- PC (Windows, Mac OS, Linux)
- 웹 브라우저 (Google Chrome or Mozilla Firefox 권장)
- 인터넷 연결
- [AWS 계정](https://aws.amazon.com/console/)

![Preferred web browsers](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/prerequisites/web-browsers-small.svg)

Cloud Club의 캠프나 행사의 경우 임시 AWS 계정이 제공될 것입니다. 기존 계정을 사용하셔도 좋지만, 제공되는 계정을 활용하시는 것을 매우 권장드립니다. 실제 운영 중인 Workload가 있는 계정은 사용을 자제하는 것이 좋습니다.

> ⚠️ 워크숍 과정에서 각 단계들을 수행하면 AWS 서비스가 프로비저닝되어 **요금이 발생** 하게 됩니다.  제공된 계정의 경우 이러한 요금은 처리될 것이므로 문제가 되지 않습니다. 하지만 본인의 계정을 사용하는 경우, 비용이 발생할 수 있다는 점을 조심해야합니다. 더 이상 필요하지 않을 때 실행 중인 서비스를 종료하거나 Amazon S3에 저장된 데이터 객체를 삭제하는 등의 조치를 취해야 합니다. 이렇게 하면 워크숍 완료 후 요금이 계속 발생하는 것을 방지할 수 있습니다.



## 여러분의 도전과제!!

![iam-computer-lab](https://static.us-east-1.prod.workshops.aws/public/856f008e-b000-462c-b14e-2b12e35d7697/static/images/iam/proposal.png)

 학교에서, 컴퓨터 전공 교수님은 강의에서 사용하는 애플리케이션을 실행하는 데 로컬 장비를 사용하는 것에 익숙합니다. 컴퓨터 공학과의 성적표와 학과의 기념품을 판매하기 위한 웹 포털은 옷장에 보관된 먼지 쌓인 유닉스 박스에서 호스팅되고 있습니다. 이제 이 장비는 노후화의 징후를 보이기 시작했습니다.

 소프트웨어는 업그레이드가 필요하고, 기계는 자주 충돌하여 재부팅이 필요할 뿐만 아니라 보안도 취약합니다. 비밀번호는 필요할 때 재설정되지 않아 학생들 사이에 널리 공유되어 있습니다. 프랑스어학과에서는 학생들이 다른 시스템에 접근하기 위해 서버를 해킹하고 있습니다. 최근에는 이런 시도가 높은 성공률을 보이고 있죠! 게다가 컴퓨터 공학과의 기념품이 너무 인기가 있어 더 많은 학생들이 티셔츠와 피젯 스피너를 주문하면서 웹 포털은 점점 더 느려지고 신뢰성이 떨어지고 있습니다. 교수님은 강의의 민감한 자료를 안전하게 보호하면서 컴퓨터 공학과의 기념품 주문은 문제없이 더 많이 받을 수 있도록 조치를 취해야 한다는 것을 잘 알고 있습니다. 하지만 어떻게 해야 할까요?

*"이 애플리케이션들을 클라우드에서 실행하면 어떨까요? 유연하고, 안전하며, 비용 효율적일 뿐만 아니라 잦은 장애에 대해 걱정하지 않아도 될겁니다!"*라고 여러분이 교수님에게 제안합니다. 교수님은 가장 유능한 컴퓨터 공학과 학생인 여러분이 강의 인프라를 클라우드로 옮기는 것에 대해 매우 기뻐합니다. 이와 동시에, 여러분은 친구들이 이 클라우드 컴퓨팅 비즈니스를 이해하는 데도 도움을 줄 수 있을 것입니다. 상황을 간단하게 분석해본 뒤, 여러분은 다음과 같은 작업을 제안합니다.

> - AWS에서 제공하는 다양한 서비스를 활용한 리소스를 생성하여 클라우드 컴퓨팅의 기능을 알아보고 익숙해집니다.
> - 개별 사용자에게 권한을 부여하는 계정과 보안 제어를 통해 강의 환경에 대한 접근을 관리합니다.
> - 클라우드에 가상 네트워크를 구축하고 격리된 환경에서 애플리케이션을 개발합니다.
> - 성적부 데이터나 웹 포털에서 판매되는 학과 기념품 이미지를 위해 클라우드 스토리지를 사용합니다.

교수님은 정말 훌륭한 아이디어라 생각하며, 여러분이 강의를 위한 클라우드 컴퓨팅으로의 여정을 담당하는 것을 허락합니다. 이제 시작할 시간입니다. 먼저 환경을 안전하게 보호하는 것부터 시작해 봅시다!