# Spring Triangle (Spring 핵심 3대 요소)  
### Spring-Projects Repository인 spring-petclinic을 예제로 사용 

<br>

#### 참고자료

---
- [Spring-petClinic](https://github.com/spring-projects/spring-petclinic)
- [Spring-petClinic README](https://github.com/LeeGiCheol/spring-project-spring-petclinic/blob/main/spring-readme.md)
- [백기선 - 예제로 배우는 스프링프레임워크 입문](https://www.youtube.com/watch?v=HACQV_koAIU&list=PLfI752FpVCS8_5t29DWnsrL9NudvKDAKY)
---

<br>

### `Spring Triangle (Spring 핵심 3대 요소)`  
    1) IoC (Inversion of Control)  
    2) AOP (Aspect Oriented Programming)  
    3) PSA (Portable Service Abstraction)  
    
1. Inversion of Control, Dependency Injection
    1) IoC의 개념
    2) DI를 받는 방법 3가지
        1) Field에 Autowired Annotation
        2) 생성자로 주입
        3) Setter를 통해 주입  
        
2. AOP (Aspect Oriented Programming)
    1) AOP 구현 방법
        1) 컴파일 A.java --- (AOP) --- A.class (AspectJ)
        2) 바이트코드 조작 A.java -> A.class --- (AOP) ---> 메모리 (AspectJ)
        3) 프록시 패턴 (Spring AOP가 사용하는 방법)
            - 실제 기능을 수행하는 객체 대신 가상의 객체를 사용해 로직의 흐름을 제어하는 디자인 패턴
            - 흐름제어만 할 뿐 결과값을 조작하거나 변경시키면 안된다
            
3. PSA (Portable Service Abstraction)
    1) Service Abstraction
        - Spring은 Servlet Application임에도 불구하고 Servlet은 전혀 존재하지 않는다.<br>
          예를들어 @GetMapping, @PostMapping과 같은 Annotation을 사용해서 해당 Method가 처리할 수 있도 요청을 Mapping한다.<br>
          이처럼 내부적으로 Servlet이 동작하는 것을 추상화시켰다.<br>
          이렇게 추상화를 통해 기술을 숨기고 편의성을 제공하는 것을 Service Abstraction이라고 한다.<br>
          Service Abstraction으로 제공되는 기술을 환경의 변화와 관계없이 일관된 방식의 기술 접근 환경을 제공하려는 추상화 구조를 PSA라 한다.
    2) @Transactional
        - Transaction은 데이터베이스의 상태를 변환시키는 하나의 논리적 기능을 수행하기 위한<br> 
          작업의 단위 또는 한꺼번에 모두 수행되어야 할 일련의 연산이다.
        - Transaction 처리를 하기 위해서는 commit, rollback과 같은 명령어를 사용해 구현해야 하지만,<br>
          @Transaction Annotation을 붙이는 것으로 transaction 처리를 쉽 할 수 있다.<br>


과제
1. /owners/find 의 검색을 lastName - firstName으로 변경
2. 검색 시 WildCard를 앞 뒤로 두기 (ex. leegicheol을 검색 시 gi 만 검색해도 나올 수 있도록)
3. h2 데이터베이스에 age 컬럼 추가. thymeleaf에도 적용
