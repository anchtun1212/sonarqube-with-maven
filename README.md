# sonarqube-with-maven
How to integrate SonarQube with your Maven projects

# Check .md file
open: https://commonmark.org/help/

# Run docker-compose file
`sudo docker compose up`

# Open SonarQube
open: http://localhost:9000/

- the default user and password are: admin/admin

# Open Jenkins
open: http://localhost:8080/

- you should insert: Administrator password

- Run: `sudo docker ps`
- Run: `sudo docker exec -it jenkins_container_id bash`
- Run: echo \`find . -name initialAdminPassword\`
- Run: `cat ./var/jenkins_home/secrets/initialAdminPassword`

# JaCoCo
open: https://www.jacoco.org/jacoco/trunk/doc/maven.html

To receive a full list of goals and available parameters you can use maven-help-plugin (go inside pom.xml folder):

`mvn help:describe -Dplugin=org.jacoco:jacoco-maven-plugin -Ddetail`

Run this: `mvn org.jacoco:jacoco-maven-plugin:prepare-agent verify org.jacoco:jacoco-maven-plugin:report`

Then go inside: /target/site/jacoco/index.html (open with browser)

#Java test coverage reports
Java test coverage reports are generated with: `mvn org.jacoco:jacoco-maven-plugin:prepare-agent verify org.jacoco:jacoco-maven-plugin:report sonar:sonar -Dsonar.jdbc.username=sonar -Dsonar.jdbc.password=password -Dsonar.host.url=http://<sonarqube-address>:9000 -Dsonar.jdbc.url=jdbc:postgresql://<postgre-address>/sonarqube`







