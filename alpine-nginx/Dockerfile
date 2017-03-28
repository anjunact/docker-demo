FROM alpine:3.5
RUN echo "http://mirrors.aliyun.com/alpine/v3.5/main/" > /etc/apk/repositories
RUN apk add --update nginx && rm -rf /var/cache/apk/*
RUN mkdir -p /run/nginx
COPY nginx.non-root.conf /etc/nginx/nginx.conf
RUN mkdir -p /usr/share/nginx/html
COPY index.html /usr/share/nginx/html/index.html

USER nobody

CMD ["nginx","-g","daemon off;"]
