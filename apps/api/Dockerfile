FROM node:14
WORKDIR /opt/app
ADD . .
RUN apt-get update
RUN apt-get upgrade
RUN apt-get install build-essential libssl-dev
RUN apt-get install nodejs -y
RUN apt-get install npm -y
RUN apt-get npm run build api -y
CMD ["node", "./dist/apps/api/main.js"]
