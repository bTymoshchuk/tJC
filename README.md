# Welcome to tJC!
To deploy the project use the following instructions:
## 1.Install and configure Apache Tomcat
- [Download and install Java 8 or later](https://www.oracle.com/technetwork/java/javase/downloads/index.html)
- [Download Tomcat Apache 9.0](http://mirror.klaus-uwe.me/apache/tomcat/tomcat-9/v9.0.24/bin/apache-tomcat-9.0.24.exe)
- Execute the downloaded file
- Select the full type of installation
- In the next window create your user and give it 'admin-gui' and 'manager-gui' roles
  - you can also create a new user after the installation pasting the following code in your `Tomcat <version>\conf\tomcat-users.xml`
  ```
  <role rolename="manager-gui"/>

  <role rolename="admin-gui"/>

  <user username="admin" password="password"
  roles="admin-gui,manager-gui"/>
  ```
- Start the Tomcat Service
  - if your Tomcat Server doesn't set up, some other application could be using tomcat ports run `netstat -a` in the command line and, if 8080 or 8005 is being used, change it in `Tomcat <version>\conf\server.xml` with any unsed port
- Go to [localhost:8080/manager](localhost:8080/manager) and log in
## 2. Clone the repository
In GIT Bash execute `git clone https://github.com/bTymoshchuk/tjc.git`
## 3. Copy the Angular app and the Spring Boot API to the Tomcat
 - Go to your Apache Tomcat installation foder
 - In `Tomcat <version>\webapps` remove `ROOT`, `tjcapi` and `tjcapi.war`(if they exist)
 - Copy `ROOT` folder and `tjcapi.war` from downloaded repository to `Tomcat <version>\webapps` folder:
## 4. Change the API URL in the Angular app
 - Go to `Tomcat <version>/webapp/tjc/index.html.`
 - In the script tag replace the value of `cfgApiBaseUrl` with the path to your api(`localhost:8080/tjcapi` by default).
## 5. Restart Apache Tomcat
