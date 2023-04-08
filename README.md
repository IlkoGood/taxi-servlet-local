
Main description:

An example of servlet-based program, over-simplified management system 
with following abilities:

Authenticate / create user aka driver, restrict access to pages;

Create and delete car manufacturers, car models, provide their listings;

CRUD drivers with assigning / unbinding corresponding cars;

Program provides minimalistic button-based interface with joke included (try to delete your authenticated driver from driver list);

Main startup steps:

Please have IntelliJ IDEA Ultimate or ability to adapt following steps on your own;

You will also need: Tomcat 9.0.50 - 9.0.73, Java SDK 17+, maven 3.8.0+, SQL DBMS (tested on MySQL)

Download this repo to destination without any gaps and non-latin symbols in path;

Create database with query provided in src/main/resources/init_db.sql;

Update src/main/java/taxi/util/ConnectionUtil.java with your database connection information;
Check for timezone in URL field (see example screenshot):

Execute mvn clean package;

Configure run with Tomcat as on screenshots, or deploy .war in a way, more convenient for you;

In case of configuring as on screenshots just wait for browser to open, otherwise check http://localhost:8080/login;
