## Start MinIo server 

```
docker run -d --name minio \
  -p 9000:9000 \
  -p 9090:9090 \
  -e MINIO_ROOT_USER=your_user_name \
  -e MINIO_ROOT_PASSWORD=your_password \
  -v minio_data:/data \
  minio/minio server --console-address ":9090" /data
```
