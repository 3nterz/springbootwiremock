![Spring boot](https://upload.wikimedia.org/wikipedia/en/2/20/Pivotal_Java_Spring_Logo.png "Spring boot") ![](hhttps://upload.wikimedia.org/wikipedia/en/2/20/Pivotal_Java_Spring_Logo.png "Spring boot")

# Local Environment Setup of Tomcat and Sprint Boot App with Embedded Wiremock (HTTP & HTTPS)

## Background information

This Spring based project contains code to demonstrate the use of Embedded Wiremock with configuration for recording mapping files from both HTTP and HTTPS target URLs and setting up appropriate keystores and truststores to establish what SSL certificate is seen when accessing the URL through wiremock and also what SSL certificates can be trusted by the wiremock server.

This code in this project provides a WAR file that can be deployed into a Apache Tomcat Server. The WAR file when deployed, programmatically starts wiremock server, and starts recording mode targeting a HTTP URL first, and calls this HTTP endpoint through Wiremock server, using RestAssured framework, in order to automatically generate the mapping files for the HTTP endpoint. The code then stops recording mode for the HTTP endpoint and resets the wiremock cache in order to move on to recording mapping files for a HTTPS URL. This HTTPS URL will be called through Wiremock server, using RestAssured framework configured with truststores and also Oauth 2 authentication.

## Software Deployment Dependencies
* Microsoft Windows
* Oracle Java JDK 8 - https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
* Apache Tomcat 9 - http://tomcat.apache.org/

## Software Development Environment
* Microsoft Windows
* Git - https://git-scm.com/
* Eclipse IDE - https://www.eclipse.org/ide/
* Apache Maven 3 - https://maven.apache.org/
* Oracle Java JDK 8 - https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

## Integrated Software Libraries
* RestAssured - http://rest-assured.io/
* Apache HTTP client - https://hc.apache.org/httpcomponents-client-ga/
* Apache Commons IO - https://commons.apache.org/proper/commons-io/
* JSON in Java - https://github.com/stleary/JSON-java
* Wiremock - https://github.com/tomakehurst/wiremock
* Spring Boot - https://github.com/spring-projects/spring-boot

# Getting Started

## Download and install JDK 8

![alt text](https://upload.wikimedia.org/wikipedia/en/thumb/3/30/Java_programming_language_logo.svg/234px-Java_programming_language_logo.svg.png "Logo")

* Go to the Oracle website to download the JDK. At time of writing instructions were available here on the Oracle website: https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html#CHDEBCCJ
* Set the `JAVA_HOME` environment variable to point to the folder the JDK was installed at. For example in Windows running the command `echo %JAVAHOME%` may return `C:\Program Files\Java\jdk1.8.0_191`

## Download, extract and install Apache Maven 3.x

![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Maven_logo.svg/512px-Maven_logo.svg.png "Spring boot")

* Steps to download Apache Maven may be found here: https://maven.apache.org/download.cgi
* Steps to install Apache Maven may be found here: https://maven.apache.org/install.html

## Download and Install Eclipse

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Eclipse_Foundation_Logo.svg/1193px-Eclipse_Foundation_Logo.svg.png "Spring boot")

* Latest version of Eclipse may be downloaded here: http://www.eclipse.org/downloads/packages/
* Steps to install Eclipse may be followed here: https://wiki.eclipse.org/Eclipse/Installation
* Configure Eclipse to use JDK 8 as an Installed JRE - https://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Ftasks%2Ftask-add_new_jre.htm
* Configure Eclipse to use above external Maven installation - in Eclipse go to Window > Preferences > Maven > Installations to see this

## Download the source code and compile the project

![](https://avatars0.githubusercontent.com/u/4571183?s=200&v=4  "Spring boot")

* Ensure Git bash is installed - https://gitforwindows.org/
* Download the source code of this repository using Git bash - https://help.github.com/articles/cloning-a-repository/#platform-windows
* Run the following command to build maven project. The –U option update the local maven repository with newest versions from remote maven repositories.

`mvn clean install -U`

* A target folder will be created if not already existing and a WAR file named WireMockSprintBootDemo.war will be generated.

## Setting up Apache Tomcat

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7b/Tomcat-logo.svg/300px-Tomcat-logo.svg.png
  "Spring boot")


## Setting up certificates and Java keystores

## Deploying WAR file to tomcat

## Checking log files

## Checking Wiremock mapping files

![](https://1.bp.blogspot.com/-7Z1EthpEr0c/WiuxpMx3PPI/AAAAAAAAC-A/Og2wGG6PZBwGzJxqyR1N_hHzcwRAWPDVQCLcBGAs/s1600/wiremock.jpg "Logo")

## Import Spring boot maven project into Eclipse

* See https://stackoverflow.com/a/36242422
