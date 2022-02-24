FROM node:lts-alpine
ENV NODE_ENV=production
ENV MONGO_HOST "host.docker.internal"
ENV ROOT_URL=http://localhost
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production && mv node_modules ../
RUN npm run build:client
COPY . .
EXPOSE 2222 80
RUN chown -R node /usr/src/app
USER node
CMD ["npm", "start"]
