- mkdir symfony-docker
- cd symfony-docker

Project Structure:    
    symfony-docker/
    ├── docker-compose.yml
    ├── Dockerfile
    ├── php.ini
    ├── nginx/
    │   └── default.conf
    └── mysql/

# Build the containers:
    - docker-compose build

# Start the containers:
    - docker-compose up -d

# Verify that the containers are running:
    - docker-compose ps

# Access the PHP container:
    - docker exec -it symfony_php bash

# Use Composer to create a new Symfony project:
    - composer create-project symfony/skeleton my_project
    (my_project isimli klasörde olmasın diyorsan yerine . koy.)
    - cd my_project


# Configure the Database
    - Edit the .env file inside your Symfony project (my_project/.env) and set the DATABASE_URL:
        * DATABASE_URL="mysql://root:root@db:3306/symfony"

- Exit (CTRL D)

- docker-compose down
- docker-compose up -d

- docker exec -it symfony_php bash
- cd my_project

- Go to http://localhost:8080


# How to WORK With Project 
- docker-compose up -d
- docker exec -it symfony_php bash
- Go to http://localhost:8080


# MYSQL Container Connect
- docker ps
- docker exec -it <container_id> mysql -u root -p (password admin)
- SHOW DATABASES;


NOTLAR:
- symfony cli'ın sunduğu ``symfony start:server`` komutuyla symfony web server çalışır 
    ancak browser'da açılmaz. (http://127.0.0.1:8000/)(Belki vardır yolu ama şimdilik skip)