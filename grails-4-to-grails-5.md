# Why should I update?

- Java 8 has reached EOL, so if we want to start using Java 11 it is important migrate to
Grails 5  that uses Groovy 3.x and supports Java 11.


- Grails 4 will be discontinued at the end of 2023, if you have plans to continue using your
application in production you need to keep your project updated.


- Grails 5 it's the most recent version of the framework, so provides an easy way to update to futures versions.


# Steps to upgrade to Grails 5

1. Update your gradle version in `gradle/wrapper/gradle-wrapper.properties`, Grails 5 is using **Gradle 7.2 and later**
   `distributionUrl=https\://services.gradle.org/distributions/gradle-7.2-bin.zip` also you can run this command `./gradlew wrapper --gradle-version 7.2`
<br><br>
2. Update your grailsVersion, gorm.version and groovyVersion in your `gradle.properties` <br> `grailsVersion=5.2.0` <br>
   `groovyVersion=3.0.7` <br> `gorm.version=7.2.0`
<br><br>
3. Update your `views-gradle` should be like this `"org.grails.plugins:views-gradle:2.3.2"`
<br><br>
4. In your `build.gradle` you need to use `implementation` instead of `compile`, `providedRuntime` instead of `provided`,
   `runtimeOnly` instead of `runtime`, `testImplementation` instead of `testCompile`
