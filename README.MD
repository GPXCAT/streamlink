# build
```bash
docker build --build-arg VERSION=6.5.0 -t jscat/streamlink .
```

# build multi platform
```bash
docker buildx build --build-arg VERSION=6.5.0 --platform linux/amd64,linux/arm64 -t jscat/streamlink:latest --push .
```

# run
```bash
docker run --rm -it \
    -v $(pwd):/app -w /app \
    jscat/streamlink -o abema.ts \
    https://abema.tv/video/episode/26-162_s3_p2 best
```

# install docker
https://docs.docker.com/engine/install/ubuntu/
```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

streamlink documentation: https://streamlink.github.io