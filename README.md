# video-health-nginx
===========

이 저장소에는 다음에 최적화 된 nginx를 빌드하기위한 Dockerfile이 포함되어 있습니다. 

- [lua-nginx-module](https://github.com/openresty/lua-nginx-module) (with
  luajit) for Lua scripting
- [nginx-rtmp-module](https://github.com/arut/nginx-rtmp-module) for live
  streaming (with on-the-fly HLS/DASH segmenting)
- [nginx-video-thumbextractor-module](https://github.com/wandenberg/nginx-video-thumbextractor-module)
  for thumb generation
- [nginx-vod-module](https://github.com/kaltura/nginx-vod-module) for
  on-the-fly video segmenting
- [nginx_upstream_check_module](https://github.com/dddpaul/docker-nginx) for
  on-the-fly add the support of upstream server health checks

The image is available on Docker Hub:
https://hub.docker.com/r/ossboard/video-health-nginx/.

### build
``` 
docker build -t ossboard/video-upstream-nginx:latest . 
```

### run
``` 
cd ~/docker-compose-test
docker-compose up -d

```
