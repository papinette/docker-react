FROM nginx:1.15.2-alpine

RUN apk --no-cache add bash

ENV PORT=80 \
    NODE_ENV=prod

EXPOSE ${PORT}

WORKDIR /var/www

COPY ./nginx.conf /etc/nginx/nginx.conf

CMD ["/bin/bash", "-c", "nginx -g \"daemon off;\""]
