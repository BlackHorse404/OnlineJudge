FROM node:8.12.0
WORKDIR /app
COPY package*.json /app
copy . /app
RUN npm install  
RUN pwd
CMD npm run build
