# OpenAPI And Vert.x Bootstrap Archetype (Work In Progress)

Following a [Contract-First API Development Approach](https://bit.ly/contract-first-api) can be daunting depending on the tools, languages, and frameworks you might like to use. This [Maven Archetype](https://maven.apache.org/guides/introduction/introduction-to-archetypes.html) is a quick-start for building a new OpenAPI driven application in [Spring Boot](https://spring.io/projects/spring-boot).

## Using This Archetype

```bash
mvn archetype:generate -DarchetypeGroupId=com.redhat.consulting \
                       -DarchetypeArtifactId=openapi-spring-archetype \
                       -DarchetypeVersion=1.0.2 \
                       -Dpackage=com.redhat.runtimes \
                       -DgroupId=com.redhat.runtimes.springboot \
                       -DartifactId=springboot-petstore \
                       -Dversion=0.0.1-SNAPSHOT \
                       -Dopenapi_app_contract_uri=https://petstore.swagger.io/v2/swagger.yaml \
                       -Dinteractive=false
```

## Current Status

- Able to generate a maven project
- Integrates OpenAPI Generator via Maven Plugin
- Generates JPA Entity classes from the OpenAPI contract
- Creates interfaces for REST Controllers

## Forthcoming Features

- Add your idea to the GitHub issues!!!
