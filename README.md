# MicroBase

MicroBase is an eShop application using .Net Core for learning microservices architecture pattern in .Net core.

This application is practice to show how the microservices architecture is used in .Net for intermediate and advance developers and can be used as a base project to develop a software using .Net core.
This project is licensed under the MIT License to permit free use of it in any application.

## Technologies and softwares

* <img src="https://cdn.worldvectorlogo.com/logos/rabbitmq.svg" width="24" height="24" style="margin-top:-12px;" /> **RabbitMQ** message broker to enable communication between microservices, but it can be configured to use another message broker.
*  <img src="https://chocolatey.org/content/packageimages/sql-server-express.2019.20190106.svg" width="24" height="24"/> **Microsoft SQL Server**
*  <img src="https://cdn.freebiesupply.com/logos/large/2x/elastic-stack-logo-png-transparent.png" width="24" height="24" /> **ELK stack** (Elasticsearch, Logstash, and Kibana): Centralized logging solution to aggregate logs from all services.
*  <img src="https://cdn.worldvectorlogo.com/logos/redis.svg" width="24" height="24" /> **Redis** : Used as a distributed shared cache.
*  <img src="https://www.docker.com/sites/default/files/d8/styles/role_icon/public/2019-07/horizontal-logo-monochromatic-white.png?itok=SBlK2TGU"  height="24" style="margin-bottom:12px"/> **Docker**

## Getting ready
After installing Docker on your machine open terminal and run commands below :

    #Redis
    docker run -it  -p 6379:6379 -v "~/projects/redis/:/usr/local/etc/redis" --name redis --rm redis
    
    #RabbitMq
    docker run -d  --restart unless-stopped  -p 15671:15671 -p 15672:15672 -p 5672:5672 rabbitmq
    
    #Enabling RabbitMq Management
    docker exec rabbitmq rabbitmq-plugins enable rabbitmq_management
    
    #ELK Stak
    docker run -p 5601:5601 -p 9200:9200 -p 5044:5044 -it --name elk sebp/elk
    
    #SQL Server
    docker run -dit --restart unless-stopped -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=1q2w#E$R' -p 1433:1433 --name mssql -d microsoft/mssql-server-linux:2017-latest


## Contributing
Pull requests are welcome.

Please refer to project's style and contribution guidelines for submitting changes and additions.

 1. **Fork** the repository on GitHub
 2. **Clone** it to your machine
 3. **Create a branch** and be sure to get the latest from "upstream"
 4. **Commit** changes to created branch
 5. **Push** your changes back up to your fork
 6. Submit a **Pull request** after reviewing your changes it'll be merged


## Authors

* **MohammadReza Ariyan** - *.Net Developer* - [LinkedIn](https://www.linkedin.com/in/mohammadreza-ariyan-5b7a28b5/)

## License
Licensed under the [MIT License](https://choosealicense.com/licenses/mit/) to permit free use.
