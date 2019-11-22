FROM node:alpine
WORKDIR '/app'
COPY ./package.json .
RUN npm install
COPY . .
CMD ["npm", "run", "start"]
# CMD is the only difference between this and Dockerfile.dev
# if you go to package.json there is a start script running index.js in container
