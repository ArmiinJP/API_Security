FROM openresty/openresty:alpine-fat

RUN mkdir /var/log/nginx
RUN mv /usr/local/openresty/nginx/conf/nginx.conf /usr/local/openresty/nginx/conf/nginx.conf.default
COPY . /usr/local/openresty/nginx/conf
RUN apk add openssl-dev
#RUN apk add git
RUN apk add gcc
RUN apk add nano
RUN apk add openssl
RUN luarocks install lua-resty-openidc

ENTRYPOINT ["/usr/local/openresty/nginx/sbin/nginx", "-g", "daemon off;"]
EXPOSE 443
