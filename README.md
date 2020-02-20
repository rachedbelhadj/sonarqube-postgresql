# Docker Compose file for Sonarqube with PostgreSQL

## Installation Docker

1. Install docker and docker-compose
1. Clone the repository

## create folders for sonarqube files and PostgreSQL

```
sudo mkdir -p /var/sonarqube/{conf,data,logs,extensions}
sudo chown -R 999:999 /var/sonarqube
sudo mkdir -p /var/sonarqube/postgres

```

## Installation

1. cd sonarqube-postgres
1. Run `docker-compose up -d`
1. Open browser and browse to <http://youripaddress:9000/>

## Installation Sonar Scanner

```
sudo chmod +x install-sonar-scanner.sh
sudo ./install-sonar-scanner.sh
```

## create link: sonar-scanner

sudo ln -s /var/opt/sonar-scanner-4.0.0.1744-linux/bin/sonar-scanner /usr/local/bin/sonar-scanner

## Execute Scann

```
sonar-scanner -D sonar.login=34e4f49bbfff24db5b48bce99a71fc5b5f4da6fb

```

## Alternatives to sonar-project.properties

If a sonar-project.properties file cannot be created in the root directory of the project, there are several alternatives:


The properties can be specified directly through the command line. Ex:

```
sonar-scanner -Dsonar.projectKey=myproject -Dsonar.sources=src1
```

The property project.settings can be used to specify the path to the project configuration file (this option is incompatible with the sonar.projectBaseDir property). Ex:

```
sonar-scanner -Dproject.settings=../myproject.properties
```
