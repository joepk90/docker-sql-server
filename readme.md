# Docker SQL Server
A simple docker setup to run a mysql server accessible via localhost.

if using this in a new project, be sure to update the following configuration settings in the docker-compose.yml file:
- container_name
- volumes
- MYSQL_DATABASE

### start docker
```sh
docker-compose up -d
```

### stop docker
```sh
docker-compose down
```

### stop docker and delete volumes (databases)
```sh
docker-compose down -v
```

### log into the container
```sh
docker exec -it docker_mysql_server /bin/bash
```

### log into the mysql shell
```sh
mysql -u root -p
```

### export the database
```sh
mysqldump -u root -p docker_mysql_database > ./databases/docker_mysql_database.sql
```

### import a database
```sh
mysql -u root -p database_name < ./databases/database_name.sql
```


## mysql connection settings
These setttings can be used in your project settings or database management application (sequel pro)
| KEY | VALUE |
| ------ | ------ |
| HOST | 127.0.0.1 |
| USER | root |
| PASSWORD | docker_root |
| PORT | 8306 |