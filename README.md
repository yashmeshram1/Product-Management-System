# Spring_boot_CRUD_project_SpringMVC_SpringDataJPA_Hibernate_MySQL_Using_Html 5_css 3_Bootstrap 4_Thymeleaf
This is Spring_boot_CRUD_project Spring MVC, Spring Data JPA, ThymeLeaf, Hibernate, MySQL using html,css and bootstrap 4 and javascript all including spring security Role based authentication

### Magic of the project :-🌟🌟🌟🌟🌟🌟

You can't inspect this website even does not possible to get any source code and copy any text and others things !!! 🌟
this is the Magic on this project.🌟🌟🌟🌟
But one announcement is  actually it can't possible to disable totally inspect on a website but possible to control some inspect way
🌟🌟

### Features of the project : = 
###problem
https://github.com/MdGolam-Kibria/Spring_boot_CRUD_projectSpringMVC_SpringDataJPAThHibernateMySQLUsingHtmlForm/blob/master/src/main/java/com/example/controlProducts/productManager/jdbc/ProductJdbcTemplateRepository.java

For Products:

1.save<br/>
2.update<br/>
3.delete<br/>
3.1: manipulate data By Using @Query annotation for my own database logic.🌟🌟<br/>
4.From validation.<br/>
5.Control inspect issues.<br/>
6.spring security <br/>
7.Role based spring security with Role based access.<br/>
8.Add searching features in this project using my MySql query basen on @Query JPQL query <br/>
9.generate high level spring security  with login and logout all security features including here <br/>
10.ignoring authentication for some controller method url access 🌟🌟 way tutorial link below <br/>
@https://github.com/MdGolam-Kibria/Spring_boot_CRUD_projectSpringMVC_SpringDataJPAThHibernateMySQLUsingHtmlForm/blob/master/src/main/java/com/example/controlProducts/productManager/springSecurity/config/WebSecurityConfig.java  <br/>
11.more comming soon<br/>

### Mysql Database :-

<img src="https://user-images.githubusercontent.com/61331272/79671958-c7f35000-81ef-11ea-88f0-1495e3768e67.png" width="500" height="300" />

### MySql Database code:-

- if you want to make your database manually use the below code :-

```MySQL 
CREATE TABLE `product` (  `id` int(11) NOT NULL AUTO_INCREMENT,  `name` varchar(45) NOT NULL,  `brand` varchar(45) NOT NULL,  `madein` varchar(45) NOT NULL,  `price` float NOT NULL,  PRIMARY KEY (`id`)) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

### **Dependencies  Pom.xml**

- From@https://start.spring.io/



		`<dependency>
		    <groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-thymeleaf</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<scope>runtime</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-jdbc</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>`
		
		
### Applications.properties := 
		
`server.port=8085
spring.jpa.hibernate.naming-strategy = org.hibernate.cfg.ImprovedNamingStrategy
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5Dialect
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto = none
spring.jpa.show-sql = true
spring.datasource.url =jdbc:mysql://localhost:3306/salesdb
spring.datasource.username = root
spring.datasource.password=413152413152
logging.level.root=WARN`

### Applications.properties  Alternative way Programmatically := 

- step 1 :  in main method : = 

```Java
@SpringBootApplication(exclude = {DataSourceAutoConfiguration.class})
```

 - step 2 : make a class and paste the below code:
 
 
 
```Java 
@Configuration
public class DataSourceConfig  {
    @Bean
    public DataSource dataSource(){
        return DataSourceBuilder.create()
                .driverClassName("com.mysql.cj.jdbc.Driver")
                .url("jdbc:mysql://localhost:3306/salesdb")
                .username("root")
                .password("413152413152")
                .build();
    }
}
```


### <h1><b>Output</b></h1>
 
### Home Screen List of Product and if you want to delete a product just Press the Delete button :- 

![image](https://user-images.githubusercontent.com/61331272/79891575-fe64e100-8422-11ea-9e33-f57ed6ed4a58.png)

### Add a new Product  :-
![image](https://user-images.githubusercontent.com/61331272/79891461-d5dce700-8422-11ea-8087-7d51d7f9f851.png)

### update a product  :- 
![image](https://user-images.githubusercontent.com/61331272/79890729-bd200180-8421-11ea-8cdc-8c17e1ab4efa.png)

<h1>after add some dependency with some criteria like <b>Role based auth and access criteria with Spring security </b> below the change..  </h1><br/>

###Create database table for user/admin/others access like below

![image](https://user-images.githubusercontent.com/61331272/80320859-c69ed480-883a-11ea-9aa0-0691036a158f.png)

#After;

#First :-

- add thymeleaf-extras-springsecurity :


	```maven
	<dependency>
		<groupId>org.thymeleaf.extras</groupId>
		<artifactId>thymeleaf-extras-springsecurity5</artifactId>
	 </dependency>
	 ```


	 
#Second :-

- add thymeleaf-extras-springsecurity url in html tag :

``` html
http://www.thymeleaf.org/extras/spring-security
```

#Third :-

- add some thymeleaf attribute like below :-
# in html,
`div sec:authorize="${hasRole(hasRole('ADMIN'))}"
  This will only be displayed if authenticated user has a role computed by the controller.
div`
details in  index.html file on action access <b>Look at that</b>
###last :-
Access denied control in code <b>Look at that</b>
<h1>finally output below</h1>

#Access denied page.
![image](https://user-images.githubusercontent.com/61331272/80320394-f9939900-8837-11ea-8424-8aaa1002d102.png)

#For user:-
![image](https://user-images.githubusercontent.com/61331272/80845122-28d84a80-8c2a-11ea-896b-dedb1d2fe801.png)

# For admin
![image](https://user-images.githubusercontent.com/61331272/80845218-6dfc7c80-8c2a-11ea-9bd6-4a1d70dfb13b.png)


<h2>Any problem see the documentation below</h2>
@https://github.com/thymeleaf/thymeleaf-extras-springsecurity


### Spring security documentations: -
```Java
-authorizeRequests(): It allows restricted access. HTTP requests are authorized before being served.
- antMatchers(): It matches the URL with given pattern.
- access(): It checks if the USER has provided role.
- formLogin(): Enables form based authentication.
- loginPage(): It specifies the custom login page URL.
- loginProcessingUrl(): It specifies the URL using which username and password is validated.
- usernameParameter(): It specifies the field name to enter user name which is used by spring security to validate. If not specified then default is username.
- passwordParameter(): It specifies the field name to enter password which is used by spring security to validate. If not specified then default is password.
- defaultSuccessUrl(): It specifies the default URL which is used by spring security after successful authentication.
- logout(): It support the logout functionality in spring security application.
- logoutUrl(): If defines the URL for logout. If CSRF protection is enabled, logout request must be POST.
- logoutSuccessUrl(): It specifies the URL which is used by spring security after successful logout.
- configureGlobal(): It configures AuthenticationManager.
```

### More update comming soon next day.......
