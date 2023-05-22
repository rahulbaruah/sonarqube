# Start

`docker compose up -d`

(Or)

`sudo docker-compose -f docker-compose.yml up`

## Install Sonarscanner

```bash
sudo mkdir /opt/sonarscanner

cd /opt/sonarscanner

sudo wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.8.0.2856-linux.zip

sudo unzip sonar-scanner-cli-4.8.0.2856-linux.zip

sudo rm sonar-scanner-cli-4.8.0.2856-linux.zip

sudo chmod +x  sonar-scanner-4.8.0.2856-linux/bin/sonar-scanner

sudo ln -s /opt/sonarscanner/sonar-scanner-4.8.0.2856-linux/bin/sonar-scanner /usr/local/bin/sonar-scanner
```

## To update default host

```bash

sudo nano  sonar-scanner-4.8.0.2856-linux/conf/sonar-scanner.properties

# sonar.host.url=https://sonarqube.example.com
```

## Create a file `sonar-project.properties` in folder what u want to scan

```yml
sonar.projectKey=laravel-app
sonar.projectName=Laravel App
sonar.projectVersion=1.0
sonar.sourceEncoding=UTF-8
sonar.host.url=http://127.0.0.1:9000
sonar.sources=./app
sonar.login=admin
sonar.password=admin
```
