# Docker Compose file for Sonarqube with PostgreMysql

## Installation Docker

1. Install docker and docker-compose
1. Clone the repository

# create folders for sonarqube files and postgres
1. sudo mkdir -p /var/sonarqube/{conf,data,logs,extensions}
1. sudo chown -R 999:999 /var/sonarqube
1. sudo mkdir -p /var/sonarqube/postgres

1. cd sonarqube-postgres
1. Run `docker-compose up -d`
1. Open browser and browse to <http://youripaddress:9000/>
