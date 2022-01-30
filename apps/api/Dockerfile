FROM node:14
WORKDIR /opt/app
ADD . .
RUN apt install npm
RUN apt npm run build api
CMD ["node", "./dist/apps/api/main.js"]