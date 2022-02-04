FROM node:14
WORKDIR /opt/app
ADD . .
RUN npm install -y
RUN apt-get npm run build api -y
CMD ["node", "./dist/apps/api/main.js"]
