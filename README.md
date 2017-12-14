# rtorrent_exporter

Containerised version of [rtorrent_exporter](https://github.com/mdlayher/rtorrent_exporter)

rtorrent_exporter is a metrics exporter for [Prometheus](https://prometheus.io/)

Make sure you set the RTORRENTADDR variable with the details to access your RTORRENT instance

---
#### 0.0.2

- 2017-03-29 :: Initial release
- 2017-12-14 :: Dramatically reduced the image size

---
#### Example Run Command

```
docker run -d -p 9135:9135 -e RTORRENTADDR="http://10.0.0.1/RPC2" b3vis/rtorrent_exporter
```

#### Docker Compose Example
```
version: "2"
services:
  rtorrent_exporter:
    image: b3vis/rtorrent_exporter
    restart: always
    container_name: rtorrent_exporter
    environment:
      - RTORRENTADDR="http://10.0.0.1/RPC2"
    ports:
      - "9135:9135"
```
---
