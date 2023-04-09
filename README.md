
<h2><img src=https://user-images.githubusercontent.com/116804521/230764634-d4e661bd-423f-4af8-ab04-cd3ceb86ce31.jpg> Taxi Management System  
<img src=https://user-images.githubusercontent.com/116804521/230764634-d4e661bd-423f-4af8-ab04-cd3ceb86ce31.jpg></h2>
 
<h4>An example of servlet-based program, over-simplified management system 
with following abilities:</h4>

Authenticate / create user aka driver, restrict access to pages;

Create and delete car manufacturers, car models, provide their listings;

CRUD drivers with assigning / unbinding corresponding cars;

Program provides minimalistic button-based interface with joke included (try to delete your authenticated driver from driver list);

Currently deployed at AWS http://13.53.243.222/index (address may be changed, feel free to write me here in GitHub);

<h3>Used stack:</h3>

InteliJ Idea, JDK, including Maven plugins, MySQL;

Basic methods of Java Reflection API to assure implementing SOLID conception;

JDBC API and SQL querries to work with DB;

HTTP Servlet and Filter implementations of Java Servlet API to process requests from user;

Apache Tomcat to deploy;

<h3>Startup steps:</h3>

Please have IntelliJ IDEA Ultimate or ability to adapt following steps on your own;

You will also need: Tomcat 9.0.50 - 9.0.73, Java SDK 17+, maven 3.8.0+, SQL DBMS (tested on MySQL);

Download this repo to destination without any gaps and non-latin symbols in path;

Create database with query provided in src/main/resources/init_db.sql;

Update src/main/java/taxi/util/ConnectionUtil.java with your database connection information;

Check for timezone in URL field (see example screenshot):

<details>
  <summary>Screenshot</summary>
<img src=https://user-images.githubusercontent.com/116804521/230735152-a1cd9112-025c-4930-9582-b6741ac51113.png>
</details>

Execute <code>mvn clean package</code>;

Configure run with Tomcat as on screenshots, or deploy .war in a way that is convenient for you;

In case of configuring as on screenshots just wait for browser to open, otherwise check http://localhost:8080/login;

<details>
  <summary>Screenshots</summary>
  <img src="https://user-images.githubusercontent.com/116804521/230735159-ac9c69a8-1c67-4af8-8562-a66e8688939c.png">
  <img src="https://user-images.githubusercontent.com/116804521/230735161-87206a30-d65c-411b-b40e-e87f643ecebb.jpg">
  <img src="https://user-images.githubusercontent.com/116804521/230735166-f78d17a7-344f-4dbe-bed5-38a4a3278fd7.png">
</details>
