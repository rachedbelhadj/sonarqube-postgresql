# Docker Compose file for Sonarqube with PostgreSQL

## Installation Docker

1. Install docker and docker-compose
1. Clone the repository

## create folders for sonarqube files and PostgreSQL
1. sudo mkdir -p /var/sonarqube/{conf,data,logs,extensions}
1. sudo chown -R 999:999 /var/sonarqube
1. sudo mkdir -p /var/sonarqube/postgres

## Installation

1. cd sonarqube-postgres
1. Run `docker-compose up -d`
1. Open browser and browse to <http://youripaddress:9000/>

## Installation Sonar Scanner

1. sudo chmod +x install-sonar-scanner.sh
1. sudo ./install-sonar-scanner.sh

## create link: sonar-scanner

sudo ln -s /var/opt/sonar-scanner-4.0.0.1744-linux/bin/sonar-scanner /usr/local/bin/sonar-scanner
