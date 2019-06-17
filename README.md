# docker-shadowsocks-libev
Shadowsocks libev image with obfs.

https://github.com/shadowsocks/shadowsocks-libev

Latest Version: v3.2.3

Useage:

```yaml
version: '2'
services:
  shadowsocks:
    image: xiocode/shadowsocks-libev
    ports:
      - "10010:8838/tcp"
      - "10010:8838/udp"
    environment:
      - METHOD="xchacha20-ietf-poly1305"
      - PASSWORD="RTYySz1uOFVpNjpWTHJFYklBTFo="
      - OBFS_OPTS="obfs=http;obfs-host=www.bing.com"
    restart: always
```
