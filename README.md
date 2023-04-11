
<h1><img src=https://user-images.githubusercontent.com/116804521/230764634-d4e661bd-423f-4af8-ab04-cd3ceb86ce31.jpg> Taxi Management System  
<img src=https://user-images.githubusercontent.com/116804521/230764634-d4e661bd-423f-4af8-ab04-cd3ceb86ce31.jpg></h1>
 
### An example of servlet-based program, over-simplified management system with following abilities:
<ul>
<li>Authenticate / create user aka driver, restrict access to pages;</li>
<li>Create and delete car manufacturers, car models, provide their listings;</li>
<li>CRUD drivers with assigning / unbinding corresponding cars;</li>
<li>Program provides minimalistic button-based interface with joke included (try to delete your authenticated driver from driver list);</li>
<li>Currently deployed at AWS <b><a href="http://13.53.243.222/index">TAXI</a></b> (address may be changed, feel free to write me here in GitHub);</li>
</ul>

## Used stack

<ul>
<li>InteliJ Idea, JDK, including Maven plugins, MySQL;</li>
<li>Basic methods of Java Reflection API to assure implementing SOLID conception;</li>
<li>JDBC API and SQL querries to work with DB;</li>
<li>HTTP Servlet and Filter implementations of Java Servlet API to process requests from user;</li>
<li>Apache Tomcat to deploy;</li>
</ul>

## Startup steps

<ul>
<li>Please have IntelliJ IDEA Ultimate or ability to adapt following steps on your own;</li>
<li>You will also need: Tomcat <code>9.0.50 - 9.0.73</code>, Java SDK <code>17.0.5+</code>, <code>maven 3.8.0+</code>, SQL DBMS (tested on MySQL <code>8.0.32</code>);</li>
<li>Download this repo to destination without any gaps and non-latin symbols in path;</li>
<li>Create database with query provided in <code>src/main/resources/init_db.sql</code>;</li>
<li>Update <code>src/main/java/taxi/util/ConnectionUtil.java</code> with your database connection information;</li>
<li>Check for timezone in URL field (see example screenshot):</li>
<details>
  <summary>Screenshot</summary>
<img src=https://user-images.githubusercontent.com/116804521/230735152-a1cd9112-025c-4930-9582-b6741ac51113.png>
</details>
<li>Execute <code>mvn clean package</code>;</li>
<li>Configure run with Tomcat as on screenshots, or deploy <code>taxi-servlet-local-1.war</code> in a way that is convenient for you;</li>
<li>In case of configuring as on screenshots just wait for browser to open, otherwise check <code>http://localhost:8080/login</code>;
<details>
  <summary>Screenshots</summary>
  <img src="https://user-images.githubusercontent.com/116804521/230735159-ac9c69a8-1c67-4af8-8562-a66e8688939c.png">
  <img src="https://user-images.githubusercontent.com/116804521/230735161-87206a30-d65c-411b-b40e-e87f643ecebb.jpg">
  <img src="https://user-images.githubusercontent.com/116804521/230735166-f78d17a7-344f-4dbe-bed5-38a4a3278fd7.png">
</details>
</ul>
