FROM node:14
WORKDIR /opt/app
ADD . .
RUN apt-get npm i -y
RUN apt-get npm run build api -y
CMD ["node", "./dist/apps/api/main.js"]
