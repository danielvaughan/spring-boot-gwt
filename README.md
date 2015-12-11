spring-boot-gwt
===============

This is a modification of Ekito's example to use GWT 2.7.0 instead of 2.6.0 and Gradle instead of Maven.

A quickstart spring boot gwt application

## What's in the sources

Quick dive in the code :

- fr.ekito.gwt.server for server side code
- fr.ekito.gwt.client for GWT client side code
- fr.ekito.gwt.client.controller contains Client Http Rest controller

The application is built upon Google Gin 

## More details

More details about the project on Ekito's blog :  http://www.ekito.fr/people/?p=4816

## Update

It has also been updated to use Spring Boot 1.3.0.RELEASE and the Gretty plugin.

There seems to be an issue between the Gretty and Spring Boot plugins in Gradle that causes and error when running the build task:

Execution failed for task ':findMainClass'.
> Could not find property 'main' on task ':run'.

This can be avoided by excluding bootRepackage. So to build and run the war in Jetty the command is:

./gradlew build jettyRunWar -x bootRepackage


