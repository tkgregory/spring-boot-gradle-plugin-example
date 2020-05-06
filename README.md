## Building

`./gradlew assemble`

This will run the `bootJar` task which builds the executable fat *jar* file.

To build a *war* file include the `war` plugin, which will then run the `bootWar` task instead.

## Running

`./gradlew bootRun`

This will execute the application by searching for a class with a `public static void main(String[] args)` method, and running it.

## Acutator endpoint

With the application running, you can hit [localhost:8080/actuator/info](http://localhost:8080/actuator/info) to get
info about the application.

## Publishing

`./gradlew publish -PmavenUser=admin -PmavenPassword=buttons123`

This will publish the output form `bootJar` to a locally running Maven repository with the provided username and password.

See [this article](https://tomgregory.com/how-to-secure-your-gradle-credentials-in-jenkins/) for how to setup a local Maven repository.