FROM alpine:edge
MAINTAINER Min Yu <yumin9822@gmail.com>

RUN echo '@community http://dl-cdn.alpinelinux.org/alpine/edge/community' >> /etc/apk/repositories \
    && apk update \
    && apk add py-gevent@community py-msgpack@community wget python \
    && rm -rf /var/cache/apk/*

RUN mkdir /zeronet \
    && cd /zeronet \
    && wget --no-check-certificate https://github.com/HelloZeroNet/ZeroNet/archive/master.tar.gz \
    && tar zxvpf master.tar.gz \
    && rm -f master.tar.gz

WORKDIR /zeronet/ZeroNet-master

CMD python zeronet.py --ui_ip 0.0.0.0
