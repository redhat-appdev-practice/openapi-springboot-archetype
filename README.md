# OpenAPI And Vert.x Bootstrap Archetype (Work In Progress)

Following a [Contract-First API Development Approach](https://bit.ly/contract-first-api) can be daunting depending on the tools, languages, and frameworks you might like to use. This [Maven Archetype](https://maven.apache.org/guides/introduction/introduction-to-archetypes.html) is a quick-start for building a new OpenAPI driven application in [Eclipse Vert.x](https://vertx.io/).

## Using This Archetype

```bash
git clone https://github.com/redhat-appdev-practice/openapi-vertx-archetype.git
cd openapi-vertx-archetype
mvn install
cd <workspace>
mvn archetype:generate -DarchetypeGroupId=com.redhat.runtimes \
                       -DarchetypeArtifactId=openapi-spring-archetype \
                       -DarchetypeVersion=1.0.0-SNAPSHOT \
                       -Dpackage=com.redhat.runtimes \
                       -DgroupId=com.redhat.runtimes.springboot \
                       -DartifactId=springboot-cms \
                       -Dversion=0.0.1-SNAPSHOT \
                       -Dopenapi.app.contract.uri=https://studio-ws.apicur.io/sharing/fb9d632f-6777-44c6-a22e-0a33d88a1d52?content=true \
                       -Dinteractive=false
```

## Current Status

- Able to generate a maven multi-module project
- Integrates OpenAPI Generator via Maven Plugin
- Generates JPA Entity classes from the OpenAPI contract
- Generates jOOQ Query DSL classes from the Hibernate/JPA entities
- Creates a *stub* Vert.x Main Verticle

## Forthcoming Features

- Allow to choose between jOOQ and Hibernate Reactive
- Allow to choose between basic Vert.x style callbacks, RxJava2, and Mutiny for async APIs
- Enable generating the Vert.x Web API Contract MainVerticle
- Add your idea to the GitHub issues!!!