# Welcome to tJC!
To deploy the project use the following instructions:
## 1. Clone the repository
In GIT Bash execute `git clone https://github.com/bTymoshchuk/tjc.git`
## 2. Copy the Angular app and the Spring Boot API to the Tomcat
 1. Go to your Apache Tomcat installation foder
 2. In `Tomcat <version>\webapps` remove `ROOT`, `tjcapi` and `tjcapi.war`(if they exist)
 3. Copy `ROOT` folder and `tjcapi.war` from downloaded repository to `Tomcat <version>\webapps` folder:
## 3. Change the API URL in the Angular app
 1. Go to `Tomcat <version>/webapp/tjc/index.html.`
 2. In the script tag replace the value of `cfgApiBaseUrl` with the path to your api.
## 4. Restart Apache Tomcat
