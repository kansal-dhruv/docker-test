1. docker pull kansaldhruv/mysql
2. docker pull kansaldhruv/rest-api-spring
3. docker pull kansaldhruv/front-end
4. docker run --name mysql-standalone -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=rest-docker -e MYSQL_USER=sa -e MYSQL_PASSWORD=pass -d -p 3306:3306 kansaldhruv/mysql
5. docker run -p 8086:8086 --link mysql-standalone:mysql -d kansaldhruv/rest-api-spring
6. docker run -it --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true kansaldhruv/front-end:latest
