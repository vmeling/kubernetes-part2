FROM nginx:alpine

ARG WWW_PATH=/var/www/arch.homework/public

COPY nginx.conf /etc/nginx/conf.d/default.conf

RUN mkdir -p $WWW_PATH && \
    touch $WWW_PATH/index.php

CMD ["nginx", "-g", "daemon off;"]

EXPOSE 80
