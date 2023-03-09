빈(BEAN)이란
=============
## 빈이란? 스프링IoC 컨테이너가 관리하는 Java 객체를 의미한다.
스프링에서 POJO를 beans라고 부른다.
#### ApplicationContext.getBean()과 같은 메서드를 통해서 직접 호출할 수 있다.

## IoC 컨테이너에서 빈을 사용하는 방법
### 1. 어노테이션을 사용
Bean을 등록하기 위해서는 @Component를 사용한다.  
직접 @Component를 사용해도 되며, @Controller, @Service, @Repository와 같은 어노테이션들도  
@Component를 포함하고 있어 자동으로 빈에 등록이된다. EX (Controller Interface 안에 @Component를 포함)
### 2. 빈 설정 파일에 직접 등록하는 방법
@Configuration과 @Bean 어노테이션을 사용한다.  


## 빈 객체의 생명주기
![image](https://user-images.githubusercontent.com/64400738/223914622-e55e9162-5e22-41f8-9e57-1932feeec690.png)  
#### 1) 컨테이너를 초기화 할 때, 가장 먼저 빈 객체를 생성
#### 2) 빈 객체 생성 후, property 태그로 지정한 의존을 설정 (의존 주입)
#### 3) 모든 의존 설정이 완료되면, 빈 객체를 초기화 (빈 객체의 지정한 메서드 호출)
#### 4) 컨테이너를 종료하면, 컨테이너는 빈 객체를 소멸 (빈 객체의 지정한 메서드 호출)

## DB Connection Pool
커넥션 풀을 위한 객체가 초기화 과정에서 DB와의 연결을 생성하고 컨테이너를 사용하는 동안  
연결을 유지시켜주고, 빈 객체를 소멸할 때 DB와의 연결을 끊어주는 방식
