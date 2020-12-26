# jenkins-docker
Dockerized jenkins-agent with docker-cli and docker-compose support. This is not a docker-in-docker solution but instead exposes the host docker daemon to be accessed by the jenkins-agent container. So, any pipeline running inside the jenkin-agent container will spawn sibbling containers instead of child containers.
