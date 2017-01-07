An example project illustrating how to use [Oracle's maven repo](https://maven.oracle.com) with gradle.

# Instructions

## METHOD 1 - credentials in build.gradle

Edit `build.gradle` and scroll down to the **METHOD 1** section.

Uncomment the `credentials` block and enter your Oracle Account credentials.

Then test if gradle can resolve dependencies from the Oracle Maven repository:

```
./gradlew resolveDependencies
```

Above command should download the Oracle JDBC driver (or verify that they've
already been downloaded).

## METHOD 2 - use maven's settings.xml and optional encryption

### Prerequisites

Before trying this method, I advise you to try it with straight maven first. See:

- [example-maven-oracle](https://github.com/robin-a-meade/example-maven-oracle)  
  `github.com/robin-a-meade/example-maven-oracle`  
  an example of how to use the Oracle Maven Repo with maven

That way you'll know that your `~/.m2/settings.xml` and, if opting to encrypt
password, `settings-security.xml`, are properly set up.


### Instructions

Edit `build.gradle`.

Uncomment the plugin at the top.

Scroll down to the **METHOD 2** section.

Verify that the `name` property matches the server id you configured for the
Oracle maven repo in your `~/.m2/settings.xml`.

Then, as above, test if gradle can resolve dependencies from the Oracle Maven
repository:

```
./gradlew resolveDependencies
```

# See also

- [example-maven-oracle](https://github.com/robin-a-meade/example-maven-oracle)  
  `github.com/robin-a-meade/example-maven-oracle`  
  an example of how to use the Oracle Maven Repo with maven
- [How to add ojdbc7 to Java web app by Gradle?](http://stackoverflow.com/questions/37783669/how-to-add-ojdbc7-to-java-web-app-by-gradle)  
  `stackoverflow.com/questions/37783669`
- [Can I use the Maven repo with Gradle?](https://community.oracle.com/thread/3899544)  
  `community.oracle.com/thread/3899544`
- [Support for Maven Repositories that use realm-based SSO](https://groups.google.com/forum/#!topic/gradle-dev/G8X_41lOIlU)  
  `https://groups.google.com/forum/#!topic/gradle-dev/G8X_41lOIlU`  
  (Includes the url workaround)

<!---
- []()
  ``
-->

