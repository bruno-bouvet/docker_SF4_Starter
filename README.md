# kit-starter-symfony-4-docker
test
docker exec -it -u sf4_mysql bash

You are right now in the mysql container as root user. You can explorer this container as you want ;)


$ docker-compose build
$ docker-compose up -d


Install Symfony 4

Now we know how use Docker, so let’s go to the PHP one and not as root, but as user : dev

mac and linux: 

docker exec -it -u dev sf4_php bash

for windows : 

winpty docker exec -it -u dev sf4_php bash


Now you are inside the php container with dev user and we have to get Symfony. Just to test, launch a php -v in this container. ;)
    So let’s go to your home :

cd /home/wwwroot/sf4

    Installation of Symfony4 with composer

composer create-project symfony/skeleton my-temp-folder

When it’s done, we will get the project to the root path.

cp -Rf /home/wwwroot/sf4/my-temp-folder/. .
rm -Rf /home/wwwroot/sf4/my-temp-folder

    Launch in your browser : localhost

-> configure database in docker-compose.yml 


_**`clean images  : docker rmi $(docker images -q) --force`**_
