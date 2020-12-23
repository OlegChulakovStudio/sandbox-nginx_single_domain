FROM nginx:1.17-alpine

LABEL Description="Nginx web service base image"

RUN apk --no-cache add shadow && \
    mkdir -p /app && \
    usermod -u 82 nginx && \
    addgroup nginx www-data && \
    chown -R nginx. /app

COPY ./ci/nginx/etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

COPY --chown=nginx ./build-api /api
COPY --chown=nginx ./build-frontend /frontend

WORKDIR "/app"

CMD ["nginx", "-g", "daemon off;"]
