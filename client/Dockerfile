# We have a multi step build here, because we first did not run react app on nginx
# We also have default.conf that makes upstream nginx listen to port 3000 instead of 80

FROM node:alpine as builder
# we write as builder to mark this phase by a name
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build
# as a result we will get /build folder in /app folder as workdir is /app

FROM nginx
COPY ./default.conf /etc/nginx/conf.d/default.conf
# set up our nginx server for it to listen to port 3000
EXPOSE 3000
COPY --from=builder /app/build /usr/share/nginx/html
# copy build file from previous step

# so here we have copied default.conf to listen to port 3000
# an app consists copying data from previous step
