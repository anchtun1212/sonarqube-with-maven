# sonarqube-with-maven
How to integrate SonarQube with your Maven projects

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
