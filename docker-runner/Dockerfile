FROM phusion/baseimage

RUN apt-get update -qq && apt-get install -qqy \
    apt-transport-https \
    ca-certificates \
    curl

RUN  curl -sSL https://get.docker.com/ | sh

RUN sed -i \
          -e 's%#DOCKER_OPTS="--dns 8.8.8.8 --dns 8.8.4.4"%DOCKER_OPTS="-H tcp://0.0.0.0:4243  -H unix:///var/run/docker.sock"%' \
          /etc/default/docker

CMD  exec /bin/bash -c "service docker start; trap : TERM INT; sleep infinity & wait"

