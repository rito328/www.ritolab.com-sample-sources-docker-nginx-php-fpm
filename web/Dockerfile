FROM nginx:1.19-alpine

# update package list
RUN apk update

# settings
COPY settings/default.conf /etc/nginx/conf.d/default.conf
