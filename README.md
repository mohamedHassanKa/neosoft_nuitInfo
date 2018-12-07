# neosoft_nuitInfo
How to use this image
Pull image
$ docker pull abdelhamid007/neosoft

Run image
$docker run -p 8080:8080 abdelhamid/neosoft
If this port is already used you can try 8081:8000 or 8082:8000

The dockerfile used for this image :
FROM node:8
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD [ "npm", "start" ]
