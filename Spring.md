## Spring Data, Spring Data JDBC & Spring Data JPA

1. What is Spring Data?
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
  
The goal of Spring Data is to make it easier to work with different kinds of databases, from traditional relational databases to NoSQL databases. Spring Data is the project which consists of multiple modules (sub-projects). Below are the three main modules widely used from Spring Data project-
  
1.	Spring Data Commons – It provides shared infrastructure across the Spring Data projects. It contains technology neutral repository interfaces as well as a metadata model for persisting Java classes. 
2.	Spring Data JDBC - Spring Data repository support for JDBC. It does NOT offer caching, lazy loading, write behind or many other features of JPA. This makes Spring Data JDBC a simple, limited, opinionated ORM.
3.	Spring Data JPA - Spring Data repository support for JPA.

  
  
</blockquote>
  
<details>
<summary> <b>Explanation</b></summary>
<blockquote>

Spring Data and the sub projects are built on top of the Spring Framework. Spring Data’s mission is to provide a familiar and consistent, Spring-based programming model for data access while still retaining the special traits of the underlying data store. It makes it easy to use data access technologies, relational and non-relational databases, map-reduce frameworks, and cloud-based data services. This is an umbrella project which contains many subprojects that are specific to a given database.
 
 
  
</blockquote>
</details>
</details>

2. What is Spring Data JDBC?
<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
 
Spring Data JDBC is the project which gives benefits of Spring Data, combined with those of JDBC-
  
1.	It provided repositories with CRUD methods out of the box i.e. it provides CrudRepository interface for generic CRUD operations on a repository for a specific type.
2.	Support for @Query annotations.
3.	Nice and easy ways to extend repositories with query methods (we can just define our interface to have e.g. findByLastName method and Spring generates it for on the fly).
4.	Support for PagingAndSortingRepository interface which is extension of CrudRepository that provides additional methods to retrieve entities using the pagination and sorting.
5.	Nice integration in the Spring infrastructure, for transaction handling, dependency injection, error translation.

 
  
  
</blockquote>
</details>

3. What is Spring Data JPA?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
 
Spring Data JPA provides repository support for the Java Persistence API (JPA). It eases development of applications that need to access JPA data sources. Just like JPA, Spring Data JPA cannot work without a JPA provider. Spring Data JPA can work with Hibernate, Eclipse Link, or any other JPA provider. Spring Data JPA does a lot of things over Spring Data JDBC
  
1.	Caching (1st, 2nd level, and query cache)
2.	Automated creation of instances from queries
3.	Navigation between entities
4.	Lazy loading
5.	Dirty checking / tracking of changes to entities

  

</blockquote>

</details>


4. What is Spring Data JPA vs Spring Data JDBC?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
  
- The key differences are listed below-
 
  | **#** | **Spring Data JPA**                                                                      | **Spring Data JDBC**                             |
| ----- | ---------------------------------------------------------------------------------------- | ------------------------------------------------ |
| 1     | Database independent and portable                                                        | Generally, Database Specific                     |
| 2     | Introduces complexity through Object-Relational Mapping                                  | Less complex, than Spring Data JPA               |
| 3     | Automatic DB schema generation based on the entities                                     | Manual DB schema generation through DDL commands |
| 5     | Query annotated with JPQL code and native SQL                                            | Query annotated with only native SQL             |
| 7     | Models relationships between entities through annotations as @OneToMany, @Embedded, etc. | No relationship modeling annotations.            |
| 8     | Caching and lazy loading                                                                 | No caching, no lazy loading                      |
| 9     | Sessions and dirty tracking                                                              | No sessions, no dirty tracking                   |
  
</blockquote>

</details>

5. What is JPA? 

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
  
 The Java Persistence API, sometimes referred to as JPA, is a Java framework managing relational data in applications using the Java Platform, Standard Edition (JavaSE) and Java Platform, Enterprise Edition(JavaEE). 

</blockquote>

</details>


6. How to use Spring Data JPA in Spring Boot Project?

<details>
<summary> <b>Show Answer</b></summary>
<blockquote>
  
There are below steps you can follow in order to incorporate Spring Data JPA into Spring Boot project-
1.	First you need to set up connection with your desired database in spring application using properties like url, driver, username, password etc.
2.	Add required dependencies in project, e.g. for maven below JPA dependency need to be added into pom.xml-

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
	<groupId>mysql</groupId>
	<artifactId>mysql-connector-java</artifactId>
	<scope>runtime</scope>
</dependency>

  
```

</blockquote>

</details>

