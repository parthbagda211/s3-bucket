## Start MinIo server 

```
docker run -d --name minio \
  -p 9000:9000 \
  -p 9090:9090 \
  -e MINIO_ROOT_USER=admin \
  -e MINIO_ROOT_PASSWORD=admin123 \
  -v minio_data:/data \
  minio/minio server --console-address ":9090" /data
```
