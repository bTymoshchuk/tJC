# Welcome to tJC!
To deploy the project use the following instructions:
## 1.Clone the repository
Execute `git clone https://github.com/bTymoshchuk/tjc.git`
## 2.Copy the Angular app and the Spring Boot API to the Tomcat
1. Run the following commands in  the Windows Command Promt:
Remove your previous apps folders(if they exist):
`cd %CATALINA_HOME%\webapps
del ROOT
del tjcapi
del tjcapi.war`
Copy tJC files:
`cd <downloaded repository path>
copy tjcapi.war %CATALINA_HOME%\webapps
copy root %CATALINA_HOME%\webapps`
Restart the Tomcat server
`cd %CATALINA_HOME%\bin\
call shutdown.bat
call startup.bat`
## 3.Change the API URL in the Angular app
1. Go to `Tomcat <version>/webapp/tjc/index.html.`
2. In the script tag replace the value of `cfgApiBaseUrl` with the path to your api.
