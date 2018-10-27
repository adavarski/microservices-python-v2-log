# simplebank
App for the Microservices

Stop all simplebank containers running

docker stop $(docker ps | grep simplebank | awk '{print $1}')

Remove all simplebank containers to prvent any name clashes

docker rm $(docker ps -a | grep simplebank | awk '{print $1}')

Start all services

docker-compose up --build --remove-orphans
