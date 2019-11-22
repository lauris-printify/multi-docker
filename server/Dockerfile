FROM node:alpine
WORKDIR '/app'
COPY ./package.json .
RUN npm install
COPY . .
CMD ["npm", "run", "start"]
# again, we just change CMD
# It is indeed almost same as Dockerfile.dev, but it is because unlike react server
# express one does not come with lots of testing tools etc.
