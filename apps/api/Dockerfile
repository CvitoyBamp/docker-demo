FROM node:14
WORKDIR /opt/app
ADD . .
RUN apt-get update
RUN apt-get upgrade
RUN apt-get install nodejs
RUN apt-get npm run build api
CMD ["node", "./dist/apps/api/main.js"]
