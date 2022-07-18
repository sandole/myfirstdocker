# docker-example
Demonstrates how to pack a nodejs app into a docker container

Sequence of docker commands:

docker build -f Dockerfile -t fun-docker .

docker run -d -p 8080:8080 fun-docker

(optional) docker ps

Check out your application at localhost:8080

Pushing Docker image:

Go to hub.docker.com and change your repository to private
In your shell do:
docker images

REPOSITORY              TAG       IMAGE ID         CREATED           SIZE
verse_gapminder_gsl     latest    023ab91c6291     3 minutes ago     1.975 GB
verse_gapminder         latest    bb38976d03cf     13 minutes ago    1.955 GB
rocker/verse            latest    0168d115f220     3 days ago        1.954 GB

docker tag bb38976d03cf dockhubusername/verse_gapminder:mytag

docker login docker.io

docker push dockhubusername/verse_gapminder:mytag