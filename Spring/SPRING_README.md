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
- 스프링 부트 정적 컨텐츠 기능
- 