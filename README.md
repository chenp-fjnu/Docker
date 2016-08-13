# Docker
#dotnet Commands:
* dotnet build
* dotnet run
* dotnet test
* dotnet restore

***
#Docker 
## Wiki:
* https://yeasy.gitbooks.io/docker_practice/content/dockerfile/index.html

## Commands:
* docker images
* docker ps
* docker run [imagename]
    * Samples:
        * docker run hello-world
        * docker run -it ubuntu bash
        * docker run -d -p 80:80 --name webserver nginx
* docker build -t [imagename] .
    * Samples:
        * docker build -t webapiframe .
> imagename should be lowercase!!!
* docker tag [imageid] [dockeraccount]/[imagename]:[version]
    * Samples:
        * docker tag 7d9495d03763 pc45025/webapiframe:latest
* docker login --username=[dockeraccount] --email=[dockeraccount_mail]
* docker push [dockeraccount]/[imagename]
    * Samples: 
        * docker push pc45025/webapiframe
* docker rmi -f [imageid]|[imagename]
    * Samples:
        * docker rmi -f 7d9495d03763
        * docker rmi -f docker-whale

* docker-compose -up d 
> Run it from the folder with docker-compose.yml
> Use PowerShell if there is any issue to run docker-compose command in cmd

* docker export <container_name> -o my_container.tar