# SPRING

>**[2021-12-08]**<br>
> h2 database 다운로드 완료
> ![img.png](img.png)
> 
---

>**프로젝트 환경 설정**
> <br>
> spring.io 사이트에서 SPRING BOOT 파일을 다운받습니다.
> <br>https://start.spring.io/
> ![img_1.png](img_1.png)
> **설정**  
> 
>
> 프로젝트 선택  
Project: Gradle Project  
Spring Boot: 2.3.x  
Language: Java  
Packaging: Jar  
Java: 11  
Project Metadata  
groupId: hello  
artifactId: hello-spring  
Dependencies: Spring Web, Thymeleaf  

---
>**[2021-12-09]**<br>
**프로젝트 실행**  <br>
 ![img_2.png](img_2.png)<br>
 ![img_3.png](img_3.png)
 서버 포트 8070으로 변경했습니다.  

---

**스프링 부트 라이브러리 설정**
- 스프링 부트는 그래들 - 메이븐은
- 기본적으로 starter-web 라이브러리만 당기면, 톰캣이나 Spring-Web 등의 라이브러리를 들고오게 됩니다.<br>
<br>
- ![img_4.png](img_4.png)
- 이런식으로 무수히 많은 서로 의존관계가 있는 라이브러리들을 한 몇줄의 코드만으로 구현이 가능한 상태로 만들어줍니다.
- 스프링 부트 **톰캣 서버를 내장**
![img_5.png](img_5.png)

   ![img_6.png](img_6.png)

spring boot devtools - > https://velog.io/@bread_dd/Spring-Boot-Devtools

웹 개발 기초
- [정적 컨텐츠]
- [MVC와 템플릿 엔진]
- [API]


---
정적컨텐츠
---

### 스프링 부트 개념정리 with JPA

###  스프링이란?

#### 1. 스프링은 *프레임 워크* 이다.

- Frame : 틀 , work : 동작하다
- 너희 마음대로 만들지말고 틀을 벗어나지 않고 만들수 있게 해줄게!


#### 2. 스프링은 *오픈 소스*이다.

- 공개된 소스입니다.
- Contribute (기여) 할 수 있습니다.
- 무료입니다

#### 3. 스프링 *IoC 컨테이너*를 가진다.
#### 4. 스프링 *DI*를 지원한다..

- IoC (Inversion of controll) : 역전의 제어(주도권이 스프링에 있다.)  
- class : 설계도
>object : 실체화가 가능한 것 
>>( 누누 class { 변수   
>                    변수 }) => 누누 실체화 가능 ==> OBJECT (실체화! 게임속에 존재합니다.)
> 
> abstract class
>> 캐릭터 : 추상적인 의미 -- 게임 속에는 존재할 수 없습니다.
>>
>> 가구(abs class) : 1. 의자 : object 2. 침대 : object  
> 
> 오브젝트  
>의자  s = new 의자();  => 오브젝트의 실체화  
> 메서드마다 객체 new되는 순간 heap 메모리에 서로 다른 의자가 생성됩니다  
> 
> >스프링이 의자 , 붕어빵 , 등의 객체들을 읽어서 자동으로 Bean에 등록합니다.
![img_7.png](img_7.png)
> ####제어의 역전 예시 그림
> 
> #####DI (dependency Injection) 
> 내가 원하는 모든 class 의 method에서 의자, 붕어빵 ,사자 등의 객체를 들고와서 사용할 수 있습니다.
> 클래스에서 사용하는 의자들은 모두 같은 의자가 됩니다. ( ***싱글톤*** )  
>   
> 
- instance : 

#### 5. 스프링은 엄청나게 많은 필터를 가지고 있다.
>![img_8.png](img_8.png)
> 톰캣 안에 스프링 컨테이가 존재하는 것은 아니다.  
> 추상적인 스프링 필터 이해를 위한 그림임.  
> 톰캣 : web.xml , 스프링 : 인터셉터(AOP)
> 
#### 6. 스프링은 엄청나게 많은 어노테이션을 가지고 있다. (리플렉션 , 컴파일 체킹)

>1.컴파일 체킹 
> 어노테이션 (주석 + 힌트) << 컴파일러가 무시하지 않습니다.  
>  // 글(주석) << 컴파일러가 무시합니다. (주석+힌트)  
> Animal{ run() }  Dog 상속 
> Animal 
> run
> 
> 
> 
> 
> 
> 
> 
> 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>








 

  
  