# docker-dnsmasq

```docker build -t talma-dnsmasq .```

```SHELL
docker run \
    --name dnsmasq \
    -d \
    -p 53:53/udp \
    -p 5380:8080 \
    -v $(pwd)/dnsmasq.conf:/etc/dnsmasq.conf \
    --cap-add=NET_ADMIN \
    --log-opt "max-size=100m" \
    -e "HTTP_USER=foo" \
    -e "HTTP_PASS=bar" \
    --restart always \
    talma-dnsmasq
```
