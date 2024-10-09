![image](https://github.com/user-attachments/assets/bddeff83-4b2f-4718-8bf0-798ec9661b5c)

# All Live Young WMS README


<br>

## 팀명 소개

- All   +  Live   +  榮
- 의약품 WMS의 구축을 통해 모든 이들이 아프지 않고 젊고 꽃다운 인생을  살게 하고픈 목적을 가진 이름

## 프로젝트 소개 및 주제 선정 이유

- 이번에 참여하게된 프로젝트는 의약품 창고의 원활한 유통 관리를 위한 WMS을 구현한 프로젝트입니다.
- 2019년에 COVID-19가 유행하며 현재까지도 확진자 발생했습니다.
- 23년 5월 5일 WHO에서는 공중보건 비상사태를 해제하였고, 확진자 수는 지속적인 완화세를 보였습니다.
- 그러나 재 유행으로 인해 국내 및 해외 증상 관련 약품들이 부족한 현상 발생하였습니다.
- 따라서 의약품 재고 및 유통 관리 창고관리시스템(WMS)을 주제로 선정하게 되었습니다.

<br>

## 팀원 구성 및 소개

<div align="center">

| **이경민** | **박유미** | **최성민** | **권용빈** | **장동우** |
| :------: |  :------: | :------: | :------: | :------: |
| [<img src="https://github.com/user-attachments/assets/893611e3-6218-47d4-a2ca-37a7d1d66f82" height=150 width=150> <br/> @ceo92](https://github.com/ceo92) | [<img src="https://github.com/user-attachments/assets/10966443-bba9-4349-9650-382bf737191a" height=150 width=150> <br/> @devyumi](https://github.com/devyumi) | [<img src="https://github.com/user-attachments/assets/b8c4cac4-d93f-4043-a441-31720bbe9b47" height=150 width=150> <br/> @csm0837](https://github.com/csm0837) | [<img src="https://github.com/user-attachments/assets/0e411f18-68a7-44d8-8d5e-b210df87cb55" height=150 width=150> <br/> @EdenKwon](https://github.com/EdenKwon) | [<img src="https://github.com/user-attachments/assets/02899fa6-e9dc-49fd-925e-bdaa20015e3b" height=150 width=150> <br/> @ddw0911](https://github.com/ddw0911) |
| 팀장 | 팀원 | 침원 | 팀원 | 팀원 |
| 재고 관리, 창고 관리 | 재무 관리, 대시보드, Security | 회원 관리, 고객센터 | 입고 관리 | 출고 관리 |


</div>

<br>

## 1. 개발 환경

- Front : HTML, CSS, JavaScript, Bootstrap
- Back-end : Java, Spring Boot, ThymeLeaf, JUnit5, MySQL
- 형상관리 : Github
- 개발도구 : IntelliJ, Visual Studio, Mysql Workbench
- 협업도구 : Notion, Slack, Google Docs, Google Sheet, Zoom
<br>

## 2. 채택 프레임워크

#### Mybatis
- JPA와 달리 SQL 쿼리를 직접 작성할 수 있어 개발자들이 데이터베이스를 쉽게 다룰 수 있는 ORM(Object-Relational Mapping)입니다.
- 동적 쿼리 작성이 가능합니다. 여러 입고 요청 상품을 동적으로 입력 받는 데에 적합합니다.
- SQL 쿼리와 Java 코드를 분리하여 관리할 수 있기 때문에 유지보수 측면에서 좋은 프레임워크입니다.

#### Spring Security
- 인증, 권한 부여, 비밀번호 관리, 세션 관리 등의 보안 관련 강력한 기능을 제공합니다.
- 권한 별 접근을 제한하여 사용자, 창고 관리자, 총 관리자 별로 화면을 분리할 수 있었습니다.
  

## 3. 브랜치 전략 및 컨벤션

#### Git-Flow
- Git-Flow 전략을 채택하였고 main, develop, feature 브랜치를 사용하였습니다.
    - main 브랜치는 배포 용도로 사용하였습니다. 이 때 hotfix & release 브랜치는 실제 서비스 제공을 하지 않아 활용하지 않았습니다.
    - develop 브랜치는 feature 브랜치들을 병합하는 브랜치로 활용하였습니다.
    - feature 브랜치는 각각 기능 별로 생성하여 분리 작업을 진행하였습니다.
<br>

#### 네이밍 컨벤션
- 변수 및 메서드명: camel Case
- 클래스명: Pascal Case
- 패키지 및 테이블 컬럼명: snake case

## 4. 프로젝트 구조
![image](https://github.com/user-attachments/assets/aef15a58-8a6c-409f-a81f-340e7b9b47f9)
- 설정 클래스를 담은 config
- 상수를 정의한 constant
- 도메인 객체를 정의한 domain
- 예외 처리를 담당하는 exception
- mapper 인터페이스를 선언한 mapper
- 비즈니스 로직을 처리하는 service
- 클라이언트의 요청을 처리하는 controller
- 필요한 데이터를 담아 보내주는 dto

<br>

## 5. 프로젝트 기간

### WBS

![image](https://github.com/user-attachments/assets/a862aec8-af41-4b32-a8c5-48a71c3870c8)

<br>

## 6. 입고

#### 사용자
https://github.com/user-attachments/assets/95395859-fad4-4f05-a595-7c67995181fc
- 사용자는 본인의 입고 요청 리스트를 조회할 수 있습니다.
- 사용자는 입고 요청서를 작성할 수 있습니다.
    - 이때 입고 요청 상품은 1개 품목 혹은 그 이상의 품목을 선택하여 등록할 수 있습니다.
    - 입고 요청 코드는 실제 코드 기반 트리거를 통해 등록됩니다.
- 사용자는 본인의 입고 요청서를 수정할 수 있습니다.
    - 상품 항목은 변경할 수 없고 파레트 수, 박스 개수, 제조 번호, 유효 기간만 수정이 가능합니다.
    - 상품 항목 수정을 원할 경우 삭제 후 재 등록을 해야합니다.
- 사용자는 입고 요청서를 삭제할 수 있습니다.
- 사용자는 본인의 입고 요청서가 반려되었을 때, 반려 사유를 확인할 수 있습니다.


#### 관리자
https://github.com/user-attachments/assets/27be16e3-2a91-48d4-af7f-19d96ad80dbe
- 관리자는 본인 창고에 대한 입고 요청서를 확인할 수 있습니다.
    - 단일 입고 요청서에 대한 승인을 하게되면 재고 파레트 별로 반영이 됩니다.
    - 반려를 하게 되면 반려 사유를 작성해야 하고, 반려 사유가 표시됩니다.

<br>

## 7. 트러블 슈팅

- [조회 시 null 리턴 이슈](https://velog.io/@ybinn99/%ED%8A%B8%EB%9F%AC%EB%B8%94%EC%8A%88%ED%8C%85-ResultMap)

- [다중 쿼리 Update 불가 이슈](https://velog.io/@ybinn99/%ED%8A%B8%EB%9F%AC%EB%B8%94%EC%8A%88%ED%8C%85-Bulk-Update)

<br>

## 8. 개선 목표

- 예외 처리
    - 우선 데이터를 웹으로 정확하게 전달을 우선시 하다보니 예외 처리를 제대로 하지 못하였습니다. 이 부분을 개선할 예정입니다.
- 동시성 처리
    - 하나의 입고 요청서에 대해 사용자와 창고 관리자가 접근하여 발생하는 문제에 대해 해결할 예정입니다.
    - service 트랜잭션 처리 및 mod_date를 통한 판별

<br>

## 9. 관련 링크
[ERD] https://www.erdcloud.com/d/E6iQPxSRmuLZqKYCT

[입고 유스케이스&플로우 차트] https://app.diagrams.net/#G1QmsZ-x5EELIP1d87eztQus2YOxYP_jqr#%7B%22pageId%22%3A%22tBj_1GJiwpTEB6AQOSF3%22%7D

## 10. 프로젝트 후기

우선 단순히 WMS를 구축하는 것 뿐만이 아니라 의약품 창고에 대한 WMS를 설계했다는 점이 이번 프로젝트의 핵심이었습니다. 단순 물류 시스템을 뛰어넘어 의약, 제약 분야에 대한 관심을 웹 서비스로 나타낼 수 있어 좋았습니다. 구현에 있어 아쉬움은 많았지만 웹 서비스를 처음 구축했다는 점에 의의를 두고 차차 리팩토링하는 과정을 거쳐 성장해 나가겠습니다. 최종 프로젝트에서도 의미있는  프로젝트를 바탕으로 사용자 친화적 서비스를 제공하도록 하겠습니다.

[2차 프로젝트 회고록] https://velog.io/@ybinn99/%EC%8B%A0%EC%84%B8%EA%B3%84-%EC%95%84%EC%9D%B4%EC%95%A4%EC%94%A8-2%EC%B0%A8-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%ED%9A%8C%EA%B3%A0%EB%A1%9D
