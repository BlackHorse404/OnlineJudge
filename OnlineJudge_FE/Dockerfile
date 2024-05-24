FROM node:8.12.0
WORKDIR /  
COPY package.json .  
RUN npm install  
COPY . .
EXPOSE 5173  
CMD npm run build
CMD npm run dev
