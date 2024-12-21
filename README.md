- mkdir symfony-docker
- cd symfony-docker

Project Structure:    
    symfony-docker/
    ├── docker-compose.yml
    ├── nginx/
    │   └── default.conf
    ├── php/
    │   └── Dockerfile
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

# Configure the Database
    - Edit the .env file inside your Symfony project (my_project/.env) and set the DATABASE_URL:
        * DATABASE_URL="mysql://root:root@db:3306/symfony"

- Exit (CTRL D)

- docker-compose down
- docker-compose up -d

- Go to http://localhost:8080

- docker exec -it symfony_php bash

- bin/console doctrine:database:create



