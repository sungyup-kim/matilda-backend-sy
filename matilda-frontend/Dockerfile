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
RUN mkdir -p /frontend/node_modules/.cache && chmod -R 777 /frontend/node_modules/.cache
RUN chown -R node:node /frontend/node_modules
EXPOSE 8080
CMD ["npm", "run", "serve"]
