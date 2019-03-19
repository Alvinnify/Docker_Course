FROM node:latest

ENV DB_HOST=mydb DB_PORT=3306
ENV DB_USER=root DB_PASSWORD=chanegit
ENV APP_DIR=/app APP_PORT=3000

WORKDIR ${APP_DIR}

# ADD statement below
ADD config config
ADD public public
ADD views views

ADD main.js .
ADD package-lock.json .
ADD package.json .

# Install Libs
RUN npm install

#Exposed Port
EXPOSE ${APP_PORT}

#Run App
ENTRYPOINT ["node", "main.js"]


#CMD ["${APP_PORT}"]