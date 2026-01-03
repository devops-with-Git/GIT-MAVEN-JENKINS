============
Phase-1
============

#1
	Java Build and Deployment End-To-End Workflow.

#2
Basics
	- Java program
	- manual compilation (javac filename)
	- manual Run (java class-name)

#3
What is Maven? Why we need a build tool?
	

#4
Installation
	- Download jdk and extract it to your favourite location.
	- Download Apache Maven and extract it to your favourite location.
	- Set-up below Environment variables for Maven and JDK in order to run Maven
	  and JDK commands from any directory in the system.
		1. JAVA_HOME
		2. M2_HOME
		3. PATH

Installing JDK and Maven:
=======================
  A. create $USER_HOME/.bashrc
  
  B. create below Environment variables
	export JAVA_HOME=/home/User/Directory/Directory/jdk1.8.0_191
	export M2_HOME=/home/User/Directory/Directory/apache-maven-3.6.0
	export PATH=$JAVA_HOME/bin:$M2_HOME/bin:$PATH



Load .bashrc using below command or open new ternimial
	$ source .bashrc
 
Verify Installation
	$ java -version
	$ mvn --version or mvn -v

============
Phase-2
============

PROJECT-01 --> CREATE MAVEN web application for flipkart and perform end-to-end build and deployment.

#
create one folder where we want to store our project
$ mkdir WebApplicationProjects

#
go to that created folder i.e. sourceCode 
$ cd WebApplicationProjects/

# 
After Create Maven web application project in our created directory usign below command.
$ mvn archetype:generate -DgroupId=com.GRRAS -DartifactId=GRRAS -Dversion=1.0-SNAPSHOT -DinteractiveMode=false -DarchetypeArtifactId=maven-archetype-webapp
      
	=> archetype:generate - this is generating maven project.
        => DgroupId - this is package name. 
	=> DartifactId - this is project name. 
	=> Dversion - this is version. 
	=> DinteractiveMode - keep always interactivemode is on false.
 (Note :- Here project name is GRRAS)

#
After go to the project directory
$ cd projectName/

#
After entering project directory Build the application using below Maven command
$ mvn install

Building the maven project:
-----------------------
Execute "mvn install":

	'mvn install' command executes below maven "build life cycle" phases automatically. 
	- validate
		validate project's structure
	- initialize
		prepares project with initial pre-
		requisites ex: setting properties, creating 
		necessary directory structure..etc.	 
	- compile
		compiles "main" java code.
	- test-compile
		compiles "test" java code
	- test
		Runs the test cases and generates test reports.
	- package
		creates jar/war.
	- install
		copy built artifacts i.e jar/war file into local repository $USER_HOME/.m2 
               	(for ex. cd /home/swapnil/.m2/repository/com/gamutgurus/gamutkart/1.1-SNAPSHOT$ my war file in this repository do ls after this path we will see the war/jar file                			(gamutkart-1.1-SNAPSHOT.war))

 (Note :- 1). After mvn install target folder is created in project directory.
	  2). mvn install command is used for compiles the code. )


#
After mvn install target folder is creating in project folder in this folder Check final artifact i.e GRRAS.war file in target directory 
 (For ex. (pom.xml  src  target) like this)
$ ls target 

#
Then Prepare tomcat for deployments / installation
- Download tomcat tar.gz file from apache.org site THEN 
- Extract it. THEN 
- Make sure JAVA_HOME and M2_HOME environment variable is set in .bashrc file.

#
Then copy GRRAS.war file from target folder to tomcat webapps folder means, (Deploy GRRAS.war into tomcat webapp).
$ cp GRRAS.war $TOMCAT_HOME/webapps

#
Start tomcat server
$ $TOMCAT_HOME/bin/./startup.sh

Stop tomcat server
$ $TOMCAT_HOME/bin/./shutdown.sh

#
Launch application with below URL.
http://localhost or system-IP:8080/GRRAS
[http://tomcat_server_name:8080/warfilename]

#
find IP using below command
$ hostname -i
