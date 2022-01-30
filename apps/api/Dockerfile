FROM node:14
WORKDIR /opt/app
ADD . .
RUN sudo apt install npm
RUN sudo apt npm run build api
CMD ["node", "./dist/apps/api/main.js"]