FROM node:latest
ENV DB_HOST=mydb DB_PORT=3306
ENV DB_USER=root DB_PASSWORD=changeit
ENV APP_DIR=/app APP_PORT=3000

WORKDIR ${APP_DIR}

ADD main.js .
ADD package.json .
ADD package-lock.json .
ADD public public
ADD config config
ADD views views

RUN npm install

EXPOSE ${APP_PORT}
ENTRYPOINT ["node", "main.js"]
CMD ["{$APP_PORT}"]
