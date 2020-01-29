FROM node:latest

WORKDIR /app/
COPY package.json /app/
RUN npm install 
COPY . /app/
RUN npm install -g serve
RUN npm run build 

CMD ["serve", "-s", "build"]
