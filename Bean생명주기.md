빈(BEAN)이란
=============
### 빈이란? 스프링IoC 컨테이너가 관리하는 Java 객체를 의미한다.
스프링에서 POJO를 beans라고 부른다.
#### ApplicationContext.getBean()과 같은 메서드를 통해서 직접 호출할 수 있다.

## IoC 컨테이너에서 빈을 사용하는 방법
### 1.어노테이션을 사용
Bean을 등록하기 위해서는 @Component를 사용한다.  
직접 @Component를 사용해도 되며, @Controller, @Service, @Repository와 같은 어노테이션들도  
@Component를 포함하고 있어 자동으로 빈에 등록이된다.  
