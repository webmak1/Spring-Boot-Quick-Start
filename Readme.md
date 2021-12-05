# [Java Brains] Spring Boot Quick Start [ENG, 2016]


<br/>

**YouTube:**  
https://www.youtube.com/watch?v=msXL2oDexqw&list=PLqq-6Pq4lTTbx8p2oCgcAQGQyqN8XeA1x

<br/>

### Development

<br/>

```
$ cd app
```

<br/>


```
$ curl https://start.spring.io/starter.zip \
  -d language=java \
  -d javaVersion=11 \
  -d platformVersion=2.6.1 \
  -d dependencies=web,data-jpa,derby \
  -d packaging=jar \
  -d jvmVersion=11 \
  -d groupId=org.javadev \
  -d artifactId=springbootquickstart \
  -d name=springbootquickstart \
  -d description=Spring%20Boot%20Quick%20Start \
  -d packageName=org.javadev.springbootquickstart \
  -o springbootquickstart.zip
```


<br/>

```
$ unzip springbootquickstart.zip -d ./
```

<br/>

```
$ rm springbootquickstart.zip
```

<br/>

```
$ ./mvnw spring-boot:run
```


<br/>

### Spring Boot Quick Start 29 - Making Crud Operations with Repository

<br/>

```
// CREATE
$ curl \
    --data '{
      "id":"java",
      "name":"Java",
      "description":"Java Description"
      }' \
    --header "Content-Type: application/json" \
    --request POST \
    --url http://localhost:8080/topics \
    | jq
```

<br/>

```
// CREATE
$ curl \
    --data '{
      "id":"javascript",
      "name":"JavaScript",
      "description":"JavaScript Description"
      }' \
    --header "Content-Type: application/json" \
    --request POST \
    --url http://localhost:8080/topics \
    | jq
```

<br/>

```
// GET ALL
$ curl \
    --header "Content-Type: application/json" \
    --request GET \
    --url http://localhost:8080/topics \
    | jq
```

<br/>

```
// GET BY ID
$ curl \
    --header "Content-Type: application/json" \
    --request GET \
    --url http://localhost:8080/topics/java \
    | jq
```

<br/>

```
// UPDATE
$ curl \
    --data '{
      "id":"javascript",
      "name":"Updated JavaScript",
      "description":"Updated JavaScript Description"
      }' \
    --header "Content-Type: application/json" \
    --request PUT \
    --url http://localhost:8080/topics/javascript \
    | jq
```

<br/>

```
// DELETE
$ curl \
    --header "Content-Type: application/json" \
    --request DELETE \
    --url http://localhost:8080/topics/javascript \
    | jq
```

<br/>

### Spring Boot Quick Start 31 - Adding Entity Relationship and Extending Repository

<br/>

```
// CREATE
$ curl \
    --data '{
      "id":"java-streams",
      "name":"Java Streams",
      "description":"Java Streams Description"
      }' \
    --header "Content-Type: application/json" \
    --request POST \
    --url http://localhost:8080/topics/java/courses \
    | jq
```

<br/>

```
// CREATE
$ curl \
    --data '{
      "id":"java-concurrency",
      "name":"Java Concurrency",
      "description":"Java Concurrency Description"
      }' \
    --header "Content-Type: application/json" \
    --request POST \
    --url http://localhost:8080/topics/java/courses \
    | jq
```

<br/>

```
$ curl \
    --header "Content-Type: application/json" \
    --request GET \
    --url http://localhost:8080/topics/java/courses \
    | jq
```

<br/>

```
$ curl \
    --header "Content-Type: application/json" \
    --request GET \
    --url http://localhost:8080/topics/java/courses/java-concurrency \
    | jq
```

<br/>

```
// UPDATE
$ curl \
    --data '{
      "id":"java-streams",
      "name":"Java Streams Updated",
      "description":"Java Streams Description Updated"
      }' \
    --header "Content-Type: application/json" \
    --request PUT \
    --url http://localhost:8080/topics/java/courses/java-streams \
    | jq
```

<br/>

---

<br/>

**Marley**

Any questions on eng: https://javadev.org/chat/  
Любые вопросы на русском: https://javadev.ru/chat/
