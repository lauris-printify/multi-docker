# we are building custom docker file for nginx because we use
# default.conf to configure it.

FROM nginx
COPY ./default.conf /etc/nginx/conf.d/default.conf
# by adding default.conf in dst path, we say overwrite if default.conf exists already
