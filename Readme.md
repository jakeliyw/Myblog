# Blog devOps

# Dependent
> docker  
> docker-compose

# Usage
Download this project.
```shell script
git clone https://github.com/jakeliyw/blog5.0.git
git submodule update --remote
```

First run this project.
```shell script
docker-compose up
```

Open permission of mysql remote access.
```shell script
docker ps
docker exec -it ${mysql_contianer_name} /bin/bash
mysql -uroot -proot
use mysql
GRANT ALL ON *.* TO 'root'@'%';
flush privileges;
```

Then restart docker-compose. `Ctrl + C`
```shell script
docker-compose down
docker-compose up -d
```
