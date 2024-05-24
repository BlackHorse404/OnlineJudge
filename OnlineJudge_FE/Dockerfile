FROM node:8.12.0
WORKDIR /  
COPY package.json .  
RUN npm install  
RUN npm run build
COPY . .
EXPOSE 5173  
CMD npm run dev
