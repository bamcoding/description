# 정보처리기사
# OCJP
# SQLP

안녕하세요. 자바 스프링 웹개발 6년차 이근재입니다.
작은 일이라도 한번 시작하면 끝을 보자라는 마음으로 한번 시작한 것들을 꾸준히 해 나갔고 
그 결과 프로젝트에 채택되어 좋은 성과를 이루었다고 생각합니다.
한발한발 꾸준히 해나가는것으로 성과를 쌓아나가도록하겠습니다.



# 자바
JVM 운영체제에 상관없이 실행가능
GC 자동으로 메모리 관리 안정성
객체지향언어이구요

## MVC 패턴이란?
- MVC란 모델 뷰 컨트롤러의 약자로 애플리케이션을 세가지 역할로 구분한 개발 방법론입니다
- 사용자가 URI를 호출하면 디스패처 서블릿에서 매핑된 컨트롤러를 찾아 로직을 수행하고 모델을 이용해 데이터를 가져와 뷰에 노출시켜 사용자에게 보여준다.

## TDD 
- 테스트 주도 개발은 매우 짧은 개발 사이클을 반복하는 소프트웨어 개발 프로세스 중 하나이다.
- 요구사항을 검증하는 자동화 테스트 케이스를 작성한다.
- 그 테스트 케이스를 통과하기 위한 최소한의 코드를 생성한다.
- 작성한 코드를 표준에 맞도록 리팩토릭한다.

## TDD의 장점
- 높은 퀄리티의 소프트웨어를 보장한다는 것이다.
- 에러나 버그가 없다.
- 추가적인 요구사항을 손쉽게 반영할 수 있다.
- 유지보수에 용이하다.
- 테스트 문서의 대체가능
- 재설계 혹은 디버깅 시간의 단축

## TDD의 단점
- 생산성의 저하 단발성 개발은 개발 기간이 타이트하게 잡히는 경우가 많은데 이럴떄 TDD를 적용해 뻔한 테스트 코드를 작성하고 그에 통과하기 위한 코드를 작성한다면 마치 답을 알고 푸는 문제집처럼 따분하고 비효율적이다.


## 자바 인터페이스
- 가이드 라인
- 자바의 추상화와 다형성을 이용하여 프로그램의 유지보수성을 높이기 위해서 사용한다.
- 개발시간이 단축되고 클래스간에 의존관계 업는 독립적인 프로그래밍이 가능
- 자바8부터는 디폴트 메소드, 정적 메소드 생성이 가능하다.


## 객체지향의 5원칙
- S 단일 책임 원칙
- O 개방 패쇄 원칙
- L 리스코프 치환 원칙
- I 인터페이스 분리 원칙
- D 의존관계 역전의 원칙

- 자바 5원칙 개방 패쇄의 원칙, dfs와 bfs에 대해서 설명, 라이브러리와 프레임워크의 차이점

## 자바의 접근제어자
- public 어디에서든 접근이 가능
- protected 같은 패키지 내에서 접근 가능, 상속받은 클래스에서 접근이 가능
- default 같은 패키지 내에서 접근 가능
- private 클래스 내에서만 접근이 가능

## 스프링 프레임워크만의 장점
- 스프링 프레임워크는 자주 쓰이는 오픈소스 라이브러리의 집합 혹은 뼈대라고 볼 수 있다.
- 기존에 초기 개발 환경 구성에 시간이 단축되어 생산성이 높다.
- AOP, DI, IOP라는 특징이 있다.

## 디자인패턴 

## 리액티브 프로그래밍


## 런타임
- .java Source code파일은 컴파일러가 .class byte code로 변경해준다.
- Class Loader가 런타임 데이터 영역으로 로딩시킴 프로그램 실행
- 메소드, 힙, 스텍, 레지스트, 네이티브 매소드 스택

## 컬렉션이란 무엇인가
해당 객체는 여러 원소들을 담을 수 있는 자료구조.
데이터의 모아서 사용하는 자료구조 입니다.
### 리스트
- 어레이리스트,링크드리스트가 있다. 리스트는 배열과 비슷한 자바의 자료형으로 배열보다 편리한 기능을 가지고 있다
- 어레이리스 자바의 백터를 개선한 배열로 구현된 리스트입니다.
- 링크드리스트는 다음 노드의 주소를 기억하고 있는 리스트로 배열에 비해 삽입과 삭제가 간단하다는 장점이 있습니다.
- 하지만 탐색의 경우에는 첫번째 노드부터 탐생해 나가기 때문에 느리다는 단점이 있습니다.

### 맵
- 해시맵, 트리맵, 링크드해시맵이 있는데 해시맵을 일반적으로 사용합니다.
- 해시맵은 해시테이블을 사용하며 키값에 해시함수를 적용하여 나온 인덱스에 값을 저장하는 식입니다. 중복을 허용하지 않으며 순서가 없습니다.
- 트리맵은 레드 블랙트리 자료구조를 사용한 맵이고 트리구조이기 때문에 어느정도 순서가 보장된다.
- 링크드해시맵은 링크드리스트로 구현된 맵입니다.

### 셋
- 해시셋은 해시맵에서 키값이 없는 자료형
- 트리셋
- 링크드해시셋

### 스택과 큐
- 데이터를 기록하는 자료구조이며
- 큐는 선입선출, 스택은 후입선출입니다.

### 어레이와 어레이리스트의 다른점
- 어레이는 렝스 변수 어레이리스트는 사이즈
- 어레이는 크리가 고정
- 어레이는 기본형 참조형 변수를 담을 수 있다.

## 해시테이블이란?
해시 테이블은 키와 벨류로 데이터를 저장하는 자료구조 중 하나로 내부적으로 배열을 사용해서 데이터를 저장한다.
해시함수를 적용해 인덱스를 생성하고 인덱스를 사용해 벨류를 저장하거나 검색한다.

## 오버라이딩과 오버로딩
- 오버라이딩: 부모 클래스의 기능을 재정의한 것, 추상화 메소드를 재정의 할 때,
- 오버로딩: 상속과 관련이 없습니다. 같은 이름의 메소드를 형태가 다르게 생성할 수 있다. 파라미터가 다르거나 리턴 값이 다르거나

## 싱크로나이즈드
- 멀티스레드 환경에서 여러 스레드가 동일한 리소스에 접근하려고 하는 경우 동시성 문제로 인해서 예기치 않은 결과를 생성할 수 있다.
- 해당 예약어로 동기화 메소드 혹은 코드 블록을 지정하여 스레드 동기화를 제공한다. 스레드 사이의 실행순서 제어
- 오브젝트의 인스턴스에 모니터(열쇠)라는 개념이 있다. 열쇠가 하나여야한다.

# 스프링, 스프링부트

## 스프링 DI
- 스프링이 다른 프레인워크와 차별화되어 제공하는 의존 관계 주입 기능
- 객체를 직접 생성하는 게 아니라 외부에서 생성한 후 주입시켜주는 방식이다.
- 모듈 간의 결합도가 낮아지고 유연성이 높아진다.
- 스프링에서는 객체를 빈이라고 부르며 프로젝트가 실행될때 사용자가 빈으로 관리하는 객체들의 생성과 소멸에 관련된 작업을 자동적으로 수행해주는데 객체가 생성되는 곳을 스프링에서는 빈 컨테이너라고 부른다.

## 스프링 IoC
- 제어의 역전이라는 의미로 말, 말 그대로 메소드나 객체의 호출작업을 개발자가 결정하는 것이 아니라 외부에서 결정되는 것을 의미한다.
- 높은 응집도와 낮은 결합도를 제공

## 스프링 AOP
- 관심의 분리라고해서 기능을 비즈니스 로직과 공통 모듈로 구분한 후에 개발자의 코드 밖에서 필요한 시점에서 비지니스 로직에 삽입하여 실행되도록 한다.
- 핵심관점 + 횡단관점(트랜잭션,로그,권한 체크,인증,예외처리등)으로 분리 실현
- 스프링 xml 구현 aspect는 횡단관심 advise와 실행 시점을 명시하는 조인 포인트를 설정한것 마지막으로 advise가 실행될 target 핵심로직을 포인트컷으로 설정하면 프록시 패턴으로 인해서 핵심 로직이 실행되기 전이나 후에 횡단 로직을 수행하게 된다.
- 프록시 패턴은 제어 흐름을 조정하기 위해 중간에 대리자를 두는 패턴

## 싱글턴 패턴
- 어플리케이션이 시작될 때 어떤 클래스가 최초 한번만 메모리를 할당하고 그 메모리에 인스턴스를 만들어 사용하는 디자인 패턴
- 생성자가 여러차례 호출하더라도 최초에 생성된 인스턴스를 호출하여 반환

## 템플릿 메소드 패턴
- 슈퍼클래스에 기본적인 로직의 흐름을 작성하고, 일부 변경이 필요한 부분은 서브클래스에서 추상메소드로 오버라이딩하여 사용할 수 있는 형태로 서브클래스에서 필요에 맞게 이를 구현하여 사용하는 디자인 패턴이다
- 중복을 최소화할 때 사용합니다.
- JPA가 해당 패턴 방식으로 구현되어 있습니다.

## 팩토리 메소드 패턴
- 팩토리 메소드 패턴이란 객체 생성 처리를 서브 클래스로 분리하여 처리하도록 캡슐화 패턴입니다.
- 객체의 생성 코드를 별도의 클래스 메서드로 분리함으로써 객체 생성의 변화에 대비할 수 있다.
-
-

## 스프링과 스프링 부트의 차이점
- 엔터프라이즈 애플리케이션을 보다 쉽게 만들 수 있다. 시간비용이 단축되어 생성성이 좋다.
- DI, IOC 느슨한 결합도 높은 응집도를 제공한다. 
- AOP로 로깅, 트랜잭션 처리를 공통으로 관리할 수 있게 해준다.

## 스프링 부트
- 최소한의 설정으로 스프링 프레임워크를 사용하게 해준다.
- 스프링부트 스타터라는 의존성을 통해서 자동설정, 버전관리가 가능하다.
- 클래스와 멤버변수,메소드에 컴포넌트 스캔, 오토와이어드 등의 어노테이션을 통해서 스프링부트가 알아서 설정을 해준다.  @EnableAutoConfigration

## 메이븐과 그래이들의 특징
- 자바의 빌드 관리 툴입니다. 프로젝트에 필요한 xml, properties, jar 파일은 인식하고 빌드해주는 도구
- 소스 코드를 컴파일, 테스트, 정적분석 등을 하여 실행가능한 앱으로 빌드해줌
- 외부 라이브러리를 참조하여 자동으로 다운로드 및 업데이트의 관리해줌
- 자바의 대표적인 빌드 도구: Ant, Maven, Gradle
### Ant
- XML기반의 빌드 스크립트
- 자유로운 빌드 단위 지정
- 간단하고 사용하기 쉬움
- 대규모 프로젝트에서 복잡해지는 경향이 있음
- 라이프 사이클이 없어서 빌드 순서를 개발자가 재정의 해야함
### 메이븐
- 예전에는 ant를 사용하고 있었는데 이것을 대체하기 위해서 만들어졌습니다.
- pom.xml 파일에서 라이브러리를 관리할 수 있다. xml 기반의 빌드 스크립트에 라이프 사이클 도입됨
- 참조한 외부 라이브러리에 연관된 다른 라이브러리도 자동으로 관리됨.
- 기존에 사용하던 Ant는 빌드의 기능만 가지고 있음. 그외에는 개발자가 관리해야 했었다.
- 자동으로 라이브러리를 관리해주는 기능이 추가된 메이븐을 사용하게 되었습니다. 다운받아 사용하던 라이브러리에 변동 사항이 있으면 자동으로 업데이트하여 적용됨
### 그래이들
- 그루비 스크립트를 황용한 빌드 관리 도구
- 안드로이드 프로젝트의 표준 빌드 도구이며 멀티 프로젝트의 빌드에 최적화되어 있다.
- 메이븐에 비해 더 빠른 처리속도를 가지고 있으며 간결한 구성이 가능하다.
- build.gradle

## 어노테이션에 대해서 아는것


# 관계형 데이터 베이스
## 1.정규화
노멀라이제이션
데이터 상에서 중복을 줄이는 작업
데이터가 꼬이는 것을 방지하기 위해 테이블을 분리하는 작업
이련의 작업으로 무결성을 유지하고 디비의 저장 용량을 줄일 수 있습니다.
### 제1 정규화 위배, 원자성
- 모든 속성은 반드시 하나의 값만 가져야 한다.
- 다중 값을 가진다 [이근재|인스타,네이버,페이스북,구글]
- 반복 그룹을 가진다 [이근재|인스타|네이버|페이스북|구글]
- 1:N관계 직원과 SNS 테이블로 분리
### 제2 정규화
- 모든 속성은 반드시 모든 기본키에 종속되어야 한다.
- [주문코드|주문수량|상품코드|상품명]
- 주문이 발생하지 않으면 음료 입력 불가 -> 입력 이상
- 음료명이 변경될 경우 해당되는 주문 데이터 로우를 업데이트 해야합 -> 수정 이상
- 음료 삭제 시 주문까지 삭제 -> 삭제
- 1:N관계 음료와 주문 테이블로 분리
### 제3 정규형
- 기본키가 아닌 모든 속성간에는 서로 종속 될 수 없다.

## 2.무결성
무결성이란 관계형 데이터베이스에서 데이터의 정확성과 일관성을 보장하기 위한 제약 조건을
- 개체 무결성과 참조 무결성이 있습니다.
- 개체 무결성은 기본키를 구성하는 속성은 널이나 중복값을 가질 수 없다. 유일하게 식별할 수 있는 키어야 한다.
- 참조 무결성은 외래키 값은 널이거나 부모 테이블의 기본키 값과 동일해야 한다.

## 3.트랜잭션
- 여러 쿼리를 논리적으로 하나의 작업으로 묶어주는 것
- 거래가 일어날때 구매자의 계좌에서 출금하고 판매자의 계좌에 입급한다.
- 2개의 업데이트 쿼리로 이루어지는데 쿼리가 수행되는 도중에 서버가 다운되어 1개의 쿼리만 수행되는 경우를 방지하기 위해서 트랜잭션이 나왔다.
- 쿼리들이 한번에 실행되거나 실행되지 않게 하는것 데이터상 안정성을 보장한다.
- 커밋과 롤백
- ACID 트랜잭션이 안전하게 수행된다는 것을 보장하기 위한 성질 
- [원자성 Atomicity] 모두 반영되거나, 전형 반영되지 않아야 한다.
- [일관성 Consistency] 작업처리결과는 항상 일관성 있어야 한다. 제약 조건을 만족해야한다.
- [독립성 Isolation] 둘 이상의 쿼리가 묶여서 작업되는 와중에 다른 클라이언트가 끼어들면 안된다.
- [지속성 Durablity] 트핸잭션이 성공적으로 완료되었으면 결과가 영구히 반영되어야 한다.

독립성을 보장하기 위해서는 100개의 클라이언트가 접근할 경우 순차적으로 처리하여 동시성이 떨어진다.
이 때 격리레벨을 조정하여 동시성을 높일 수 있다.
- READ-UNCOMMITTED 커밋되지 않았지만 변경된 사항을 다른 클라이언트에서 조회할 수 있다. (DIRTY READ) 문제가 발생합니다. 트랜잭션 무효
- READ-COMMITTED 트랜잭션 이전 혹은 완료의 데이터에 접근할 수 있다. 서로 다른값이 조회(non-repeatable read)
- REPEATABLE-READ Phantom read
- SERIALIZABLE 성능은 가장 떨어지지만 ACID가 보장된다.

## 4.인덱스
보통 인덱스를 타면 조회가 빨라진다.
인덱스의 종류에는 비트리, 클러스터드 인덱스, 논 클러스티드 인덱스가 있습니다.
우리가 흔히 사용하는 인덱스는 비트리 인덱스하고 한다.

테이블을 생성할때 오브젝트를 생성한다고 하는데 테이블과 매핑된 하나의 오브젝트가 생성되는 것이다.

인덱스는 저장방식이 인덱스 컬럼 방식으로 소팅되어 저장된다.
보통 테이블은 데이터가 흩어져서 저장되어 있어서 테이블 풀스캔으로 데이터량이 많을수록 시간이 오래걸린다.
특정 조건의 데이터를 검색할 때 시작점을 지정해서 거기서부터 데이터를 검색할 수 있다.
인덱스에서 먼저 데이터를 찾고 테이블에 매핑되어 있는 곳으로 가서 찾는다.

매핑 방식은 객체지향에서 포인트처럼 인덱스가 테이블 블락에 주소를 가지고 있다.
블락은 데이터가 저장되는 최소 단위이고 거기엔 테이블의 데이터 로우단위로 저장되어 있다.
where order by에 사용할 컬럼에 대해 인덱스를 생성하면 효율정이다.
단일 컬럼, 결합 컬럼 인덱스를 생성하면 효율적.

셀렉트는 빠르지만 인서트와 업데이트는 느려지므로 마구잡이로 생성하면 안된다. 

### Cardinality(기수성)
- 인덱스를 생성할 때 속성에 대해서 비교하는 기준입니다.

## 5.조인
관계형 데이터베이스에서 여러개의 테이블을 묶어서 조회하는 기능
이너조인, 아우터조인
네스티드 루프 조인
솔트 머지 조인
해쉬 조인 - 대용량 데이터 처리를 할때 좋다.

## 6.옵티마이저의 역할
쿼리를 수행할 때 최적의 수행경로를 찾아서 수행한다.
로지컬 옵티마이저 최정의 경로
피지컬 옵티마이저 비용계산
잘못된 통계정보로 인해 잘못된 수행계획으로 수행될 수 있는데 이럴 경우
힌트를 사용해서 올바른계획으로 수행할 수 있도록 두움을 줄 수 있다.


## 리액티브 프로그래밍이란 무엇인가
- 리액티브 시스템이라는 말이 있는데 런타임 환경에서 변화에 대응하도록 전체 아키텍쳐가 설계된 프로그래밍을 말한다. 4개의 속성이 있는데 반응성, 회복성, 탄력성, 메세지 주도 속성이 있다. 이를 구현하기 위한 방법은 여러가지 있으나 자바 유틸 컨큘런트 플로우의 자바 인터페이스에서 제공하는 리액티브 프로그래밍도 한가지 방법이다.
- 리액티브 프로그래밍은 리액티브 스트림을 사용한 프로그래밍으로 잠재적 무한의 비동기 데이터를 순서대로 처리하는 기술을 말한다.

## 암호화 기법
양방향 통신을 위해 특정 키를 가지고 복호화가 가능한 출력을 만들어 내는 것
- 대칭 암호화(DES,AES)
- 비대칭 암호화(RSA)
- 해시 암호화(MD5/SHA) - 임의의 임력을 고정된 길의이 값으로 변경
- 공개키/개인키

## OAuth
- 다른 사이트의 정보로 애플리케이션에 접권 권한을 부여하는 접근 위임을 위한 개방 프로토콜.


2022/04/18 씨제이올리브네트웍스
# 자기소개 좀 해주시겠어요?

# 이직사유

# 학점이 낮다 학점에서 성실도를 확인할 수 있는 부분이라고 생각합니다. 특별한 사유가 있나요?

# 평소에 본인의 역량 개발을 어떤식으로 운영하고 있습니까?

# 두 번째 회사로 이직했을 때 출근 거리가 있다는 것을 모르고 이직을 한 것인가요?

# 보통은 이직할 곳을 정해두지 않고 퇴직을 결정하는게 쉽지 않은 결정인데 특별한 사유가 있는가?

# 공백 기간이 3개월 정도되었는데, 어떻게 준비하고 있는가?

# 정확하게 어떤 수준의 공부를 하고 있는 것인가?

# 휴면처리자동화 프로젝트를 진행하셨는데 EAI로 개발한 사유가 궁금하다. SQL과 힌트에 대한 간략한 설명.

# IT개발자는 무엇을 하는 사람이라고 생각하시나요?


