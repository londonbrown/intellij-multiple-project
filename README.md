# What is this?

An example of how to build IntelliJ plugins with [gradle-intellij-plugins](https://github.com/JetBrains/gradle-intellij-plugin) using a multi project setup.
This allows you to, for example, have a project specific to community and another project that extends that and is
intended for ultimate.

# How does it work?

## Profiles
There are profiles configured by IntelliJ version in [buildSupport/intellijProfiles.groovy](buildSupport/intellijProfiles.groovy)

This determines how the project will build for a specific version (plugin versions, build to use, etc)

When running `./gradlew`, you can specify `-Pprofile=2021_2` to run `2021_2` profile. If no profile is specified, 
`2021_1` is selected. Additionally, you can set this profile property in [gradle.properties](gradle.properties)

