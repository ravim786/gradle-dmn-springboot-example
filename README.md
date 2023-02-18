This is sample kogito project which build through gradle. The gradle script is just a wrapper around the maven build. There are additional plugins to generate swagger.json, packages dmn files in a seperate jar which can be opted out if you don't need it

The gradle build only publishes the dmn artifacts to nexus. the whole springboot fat jar is not published as needs to be packaged into a docker and pushed to artifactory/dockerhub.

Note: 
* The build from int branch will strip off '-SNAPSHOT', from the version.
* Provide the javaHome path in gradle.properties, if not the script picks from systems path 
* The default version is set to '1.0.0-SNAPSHOT' in gradle.properties

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
* Gradle 
   * gradle clean build -Pversion=1.0.0
* Maven
   * mvn clean install -DappVersion=1.0.0

Run Command
* Gradle 
   * gradle clean build bootRun
* Maven
   * mvn clean spring-boot:run

Swagger
* http://localhost:8080/swagger-ui.html
