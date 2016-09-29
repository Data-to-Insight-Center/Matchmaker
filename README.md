Matchmaker 
============

Matchmaker is a recommendation tool that selects repositories for depositing a Research Object using Repository and People information.

Steps to build:
---------------
1) Checkout the SEAD-Monitoring tool from Github and build it using Maven
~~~
https://github.com/Data-to-Insight-Center/Curbee/tree/master/services/sead-monitoring
mvn clean install -DskipTests
~~~
2) Checkout the Matchmaker repository from Github
~~~
git clone https://github.com/Data-to-Insight-Center/Matchmaker.git
~~~
3) Move the to root directory and execute following command.
~~~
mvn clean install -DskipTests
~~~
This should build all module needed for the Matchmaker service.

Steps to deploy on Tomcat:
--------------------------

1) Copy the following .war files from relevant target directory into TOMCAT_HOME/webapps.
~~~
sead-mm.war
~~~

2) Fix the endpoint URL in following configuration file under webapp.
~~~
sead-mm/WEB-INF/classes/org/sead/matchmaker/default.properties
~~~

3) Start the server.

Now the API should be accessible through the following URL.
~~~
http://host:port/sead-mm/..
~~~

Full documentation of PDT API is available at https://github.com/Data-to-Insight-Center/Matchmaker/wiki/API-Documentation
