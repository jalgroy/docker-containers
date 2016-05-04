## Bitcoind docker container

Build:
```
docker build -t bitcoind .
```

Run:
```
docker run -d --name bitcoind -p 8333:8333 -v /path/to/storage:/data bitcoind
```
