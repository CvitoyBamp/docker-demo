FROM node:14
WORKDIR /opt/app
ADD . .
RUN apt-get update
RUN apt-get upgrade
RUN rm /var/lib/apt/lists/*
RUN rm /var/cache/apt/*.bin

RUN VERSION-NAME=$(lsb_release -c)
RUN y=$(echo $VERSION-NAME | awk '{print $2}')
RUN echo $y
RUN cd /etc/apt/sources.list.d
RUN touch docker_test.list
RUN echo "deb https://apt.dockerproject.org/repo ubuntu-$y main" > docker_test.list

RUN sudo apt-get install linux-image-extra-$(uname -r) 
RUN sudo apt-get update
RUN sudo apt-get install docker.io
RUN apt-get install nodejs -y
RUN apt-get install npm -y
RUN apt-get npm run build api -y
CMD ["node", "./dist/apps/api/main.js"]
