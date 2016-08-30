#alpine-zeronet
zeronet on alpine linux
Tor is enabled

#Usage
docker run -d --name zeronet_tor --restart=always -p 43110:43110 -p 15441:15441 yumin9822/zeronet
