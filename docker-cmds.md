delete all containers: docker ps -q -a | xargs docker rm

delete all untagged images: docker rmi $(docker images | grep "^<none>" | awk '{print $3}')

