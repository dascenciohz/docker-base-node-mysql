# Docker base to Node and MySQL Project.
Docker base repository for Node projects with connection to MySQL.

1.- Add your App Node Code into "apps" folder.

2.- Set envaironment variables.

    export MYSQL_ROOT_PASSWORD=rootPass123
    export MYSQL_DATABASE=myapp
    export MYSQL_USER=myapp
    export MYSQL_PASSWORD=myappPass123
    export MYSQL_EMPTY_PASSWORD=no
    export MYSQL_EXT_PORT=3306
    export APP_EXT_PORT=3000

    * Alternatively you can create an .env file in the same path of the docker-compose.yml with the variables named above.

3.- Build and start up the service stack.

    docker-compose -f "docker-compose.yml" up -d --build

4.- Tear down service stack.

    docker-compose down

5.- (Optional) Remove MySQL data volume.

    docker volume rm mysql-data 

NOTE: If the app return error connection to MySQL, restart container to fix problem.

# Start only Node project without MySQL.

1.- Add your App Node Code into "apps" folder.

2.- Build and start up your app.

    docker-compose -f "docker-compose.yml" up -d --build myapp