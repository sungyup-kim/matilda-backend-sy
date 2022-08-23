FROM node:16.13.2
WORKDIR /frontend

COPY package*.json ./
RUN npm install

COPY . .

RUN npm install \
    moment \
    bootstrap-vue \
    axios \
    vuex \
    vuex-persistedstate

EXPOSE 8080
CMD ["npm", "run", "serve"]

