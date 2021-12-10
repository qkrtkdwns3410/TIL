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
> Animal{ run() }
Dog 상속 >> @override Animal { run ()}  >> 컴파일 (Dog)

@override fly() 사용시 >> 당연히 컴파일 단계에서 오류가 난다.
>
- 스프링 > 어노테이션 >> ~~객체 생성~~
    - @Component >> 메모리에 로딩해!
    - @Autowired >> 로딩된 객체를 해당 변수에 집어 넣어
    - @Controller >>

    ```java
    @component
    Class A { // IOC ! 스프링이 메모리에 올려야겠네! 라고 생각한다고함 (어노테이션 기법)
    ;;
    };
    ```

    ```java
    @Autowired /*>> 나중에 스프링이 B클래스를 스캔할 때 B클래스 내부에 
    어떤 친구가 있는 지 분석하는 기법 >> (리플렉션)
    
    리플렉션 :메서드 : 필드 : 어노테이션 */
    Class B{
    	//A a = new A(); >> 힙메모리에 새로운 객체를 만드는 것입니다
    	
    };
    ```

    - 런타임시에 리플렉션 기법이 시행됩니다

---

---

### 7. 스프링은 MessageConverter를 가지고 있다. 기본값은 *JSON*

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/eb091b16-b285-46ac-b919-1ec23fccb5a1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20211210%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20211210T114309Z&X-Amz-Expires=86400&X-Amz-Signature=dc88c32831a4ef8fba2f5b9a9f437361c436315371e955dbf7f3b94b1220f0a1&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

- 서로가 알아 들을 수 있는 언어로 번역하는 것이라 생각하면 편하다

- 자바 Object >> JSON >> 파이썬 Object로 변경됩니다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f23d6dc2-1f54-444b-8d33-3a1f9d5b7537/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20211210%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20211210T114401Z&X-Amz-Expires=86400&X-Amz-Signature=e8d323b0df153d20c8499741ffd6707bddebcd0318a81d90f856a6d2370fd5f0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

### 8. 스프링은 BufferedReader , BufferedWriter 를 자유롭게 사용이 가능하다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8df48b32-ddca-4635-b027-c0ac2a1784bd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20211210%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20211210T115004Z&X-Amz-Expires=86400&X-Amz-Signature=6dc68d71f53ecee7970acc1b7546c0439a2898dedc7f53fc40ce7e9b01c5642f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

-InputStream : 바이트?! >> 문자 (Char) 로 캐스팅해서 처리해야합니다. : InputStreamReader  
![img_9.png](img_9.png)

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








 

  
  