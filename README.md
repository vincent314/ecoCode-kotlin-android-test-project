# Plugin SonarQube Android Kotlin Test Project

This project aims to demonstrate how to integrate plugin-sonarqube with android project in kotlin

## Initialization

Before starting, you have to run a sonarqube instance with the creedengo Android plugin running. Please follow the documentation: https://github.com/green-code-initiative/creedengo-kotlin-android/blob/main/README.md.

On the deployed SonarQube instance, configure a project with the following properties:

- Project Key: creedengo
- Project name: creedengo
- Save the project login key somewhere

Update the [gradle.properties](gradle.properties) file with the project login key:


```yaml
# Sonar
systemProp.sonar.host.url=http://localhost:9000
systemProp.sonar.projectKey=creedengo
systemProp.sonar.projectName=creedengo

#----- Token generated
systemProp.sonar.login={INSERT_YOUR_TOKEN_HERE}
```

## Command line

```sh
./gradlew sonarqube --scan
```

Update the projectKey if you do not use creedengo as you project name in SonarQube.

## From IDE

You can launch from android studio `:app[sonarqube]`


