# Docker Compose file for Sonarqube with MySQL

## Installation

1. Install docker and docker-compose
1. Clone the repository

# create folders for sonarqube files and postgres
sudo mkdir -p /var/sonarqube/{conf,data,logs,extensions}
sudo chown -R 999:999 /var/sonarqube

1. Open terminal and cd into ./sonarqube-mysql
1. Run `docker-compose up -d`
1. Open browser and browse to <http://youripaddress:9000/>
