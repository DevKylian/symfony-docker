# Docker

### 📌 Install
- Install Docker
- git clone https://github.com/DevKylian/symfony-docker.git
- cd symfony-docker
- docker-compose up -d 
- docker-compose exec php-fpm bash
> Inside php-fpm bash
- composer create-project symfony/skeleton symfony
- mv /application/symfony/* /application
- mv /application/symfony/.* /application
- rm -Rf /application/symfony
- cd /application
> Etapes suivantes facultatives
- composer require annotations
- composer require --dev profiler
- composer require twig
- composer require orm
- composer require form
- composer require form validator
- composer require maker-bundle

### 📌 DB Sync
> In your .env file (symfony project)
- Change this 'DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name'
> Set this variable in your docker-compose.yml
- For this 'DATABASE_URL=mysql://root:root@172.28.1.3:3306/db_name'

### 📌 Docker CLI
- docker-compose down
- docker-compose up -d
> To build new Dockerfile
- docker-compose up -d --build
- docker-compose exec php-fpm bash
> Inside php-fpm bash , type this example command
- php bin/console doc:sch:crea

### 📌 Database Access
> Go to http://localhost:8080/
- User : root
- Password : root
