This is sample kogito project which build through gradle. The gradle script is just a wrapper around the maven build. There are additional plugins to generate openapi, packages dmn files in a seperate jar which can be opted out if you don't need it

The gradle build only publishes the only the dmn artifacts to nexus. the whole springboot fat just is not published as needs to be packaged into a docker and pushed to artifactory/dockerhub.

Not if you build from int branch the artifacts with be published with -SNAPSHOT.

Pre-Requisite
* gradle
* maven
* jdk11

Build Command
* gradle clean build publiToMavenLocal -Pversion=2.0.0-SNAPSHOT