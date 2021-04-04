# Create CRUD APIs in NodeJS, Express and MySQL

### docker MYSQL 연결

docker 설치
```
$ docker pull mysql
```

docker mysql 버전 지정 설치
```
$ docker pull mysql:8.0.22
```

docker 컨테이너 설치
```
$ docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=<password> --name <ungmo2-mysql> mysql:latest --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci
```

docker 컨테이너 리스트
```
$ docker ps -a
```
docker mysql 접속
```
docker exec -it <docker image name> bash

root@4cd4a2a8efbf:/# mysql -u root -p
Enter password : <password>
```




### MYSQL 8.0이상 권한 에러

error 명 : Client does not support authentication protocol requested by server; consider upgrading MySQL client

create user '{username}'@'%' identified with mysql_native_password BY '{password}';

grant all on node_mysql_crud_db.\* to '{username}'@'%';
