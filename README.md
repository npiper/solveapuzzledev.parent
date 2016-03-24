# solveapuzzledev.parent

This project is a parent pom for use in other projects, or inheritance.

## How to use the project parent in your module, project.

Use the following parent configuration:

```
<parent>
  <groupId>com.solveapuzzldev</groupId>
    <artifactId>parent.github</artifactId>
    <!-- Default starting version is 0-SNAPSHOT -->
    <version>0-SNAPSHOT</version>
</parent>
```

### Option 2:  Just copy it 

Change the `<groupId/>`, `<artifactId>` to your preferred identifiers. 

## Project Name - naming rules & convention

`<project.name>` should follow a convention of using lowercase with no spaces.

### Locations based on project name

The default reporting & project documentation go the path of the `project.name` property in Github.  Examples if the `<project.name>` was set to `tiger` would be:

* Github url:  https://github.com/npiper/tiger
* Issue tracking: https://github.com/npiper/tiger/issues
* Project pages (Github pages):  http://npiper.github.io/tiger
* scm connection: scm:git:git@github.com:npiper/tiger.git


# Default Release & Distribution

The `pom.xml` files assumes it is being built, tested, packaged and released in the environment of the [environment.buildfarm](https://bitbucket.org/n_piper/environment.buildfarm) project.

It uses the snapshot & release repositories referenced in that project.


# Configurable properties for your build

## Plugins & versions (Created 22/3/2016)

### Maven Release plugin

By default the version is v2.5.3, this is to allow the default settings
of auto versioning sub-modules. (`autoVersionSubmodules`)

### Maven checkstyle plugin - with google style checks

By default the version is v2.5.3, it is configured to use the rules from
[google style check](http://checkstyle.sourceforge.net/google_style.html)

### Corbetura reporting plugin - code coverage by tests

The reporting plugin is version 2.7, in site generation a corbetura coverage report is generated.

### Maven Enforcer plugin

The maven enforcer plugin validates minimum governance, build rules for a project. The version is 1.4.1.
The enforced minimums are shown in the next section.

## Enforced Miniumums

The maven enforcer plugin validates that the project will use the following minimum settings.

### Maven 3.1+

Don't want to maintain older versions of POM's, maven plugins.

### Java 1.7+

Want a high level of Java, good security with support for Microservices, Spring Boot & Annotations.

# F.A.Q

## How to generate the site documentation & create a structure?

## The checkstyle is too damn hard!

You can extend / overwrite the checkstyle with an 'exclusions' file.

## I don't want to corbetura cover generated java files

How to ...

