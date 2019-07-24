# docker-base-node-mysql
Docker base repository for Node projects with connection to MySQL.

1.- Add your App Node Code to "apps" path.

2.- Set envaironment variables.

    export MYSQL_ROOT_PASSWORD=rootPass123
    export MYSQL_DATABASE=myapp
    export MYSQL_USER=myapp
    export MYSQL_PASSWORD=myappPass123
    export MYSQL_EMPTY_PASSWORD=no
    export MYSQL_EXT_PORT=3306
    export APP_EXT_PORT=3000

    Alternatively you can create an .env file in the same path of the docker-compose.yml with the variables named above.


3.- docker-compose -f "docker-compose.yml" up -d --build


NOTE: If the app return error connection to MySQL, restart container to fix problem.