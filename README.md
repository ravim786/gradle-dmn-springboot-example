This is sample kogito project which build through gradle. The gradle script is just a wrapper around the maven build. There are additional plugins to generate swagger.json, packages dmn files in a seperate jar which can be opted out if you don't need it

The gradle build only publishes the dmn artifacts to nexus. the whole springboot fat jar is not published as needs to be packaged into a docker and pushed to artifactory/dockerhub.

Note: 
* if you build from int branch the artifacts with be published without -SNAPSHOT.
* please also make sure to provide the jdk11 path in gradle.properties
* also the version is defaulted to '1.0.0-SNAPSHOT' in gradle.properties

Pre-Requisite
* gradle
* maven
* jdk11
* VSCode
    * Red Hat Business Automation Bundle
    * Rest Client
    * Extension Pack for Java
    * Gradle for Java

Build Command
* gradle clean build -Pversion=1.0.0

Maven Command
* mvn clean install -DappVersion=1.0.0

Run
* gradle clean bootRun

Swagger
* http://localhost:8080/swagger-ui.html
