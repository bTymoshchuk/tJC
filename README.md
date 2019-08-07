# Welcome to tJC!
To deploy the project use the following instructions:
## 1.Clone the repository
Execute `git clone https://github.com/bTymoshchuk/tjc.git`
## 2.Copy the Angular app and the Spring Boot API to the Tomcat
1. Run the following commands in  the Windows Command Promt:\n
Remove your previous apps folders(if they exist): \n
`cd %CATALINA_HOME%\webapps`\n
`del ROOT`\n
`del tjcapi`\n
`del tjcapi.war`\n
2. Copy tJC files:
`cd <downloaded repository path>`\n
`copy tjcapi.war %CATALINA_HOME%\webapps`\n
`copy root %CATALINA_HOME%\webapps`\n
3. Restart the Tomcat server
`cd %CATALINA_HOME%\bin\`\n
`call shutdown.bat`\n
`call startup.bat`\n
## 3.Change the API URL in the Angular app
1. Go to `Tomcat <version>/webapp/tjc/index.html.`
2. In the script tag replace the value of `cfgApiBaseUrl` with the path to your api.
