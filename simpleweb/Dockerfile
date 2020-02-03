FROM node:alpine

#Make a usr/app folder and use as working directory
WORKDIR /usr/app

#copy outside node files into container
#having two copy stements for the dependencies and the other files prevents the npm install command from running uneccasarily
COPY ./package.json ./
RUN npm install
COPY ./ ./

CMD [ "npm", "start" ]

#docker build -t ikedchima/simpleweb .

#port mapping to connect lc:8080 to container:lc:8080
#   docker run -p 8080:8080 ikedchima/simpleweb