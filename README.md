#### Run docker containers
```
docker-compose up
```

#### Generate protobuf
```
protoc -I=. echo.proto --js_out=import_style=commonjs:. --grpc-web_out=import_style=commonjs,mode=grpcwebtext:.
```
