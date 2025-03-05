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
---
## Run Your Spring boot application 
```
localhost:8080
```
### Upload a File
```
curl -X POST -F "file=@sample.txt" http://localhost:8080/s3/upload
```

### List Files
```
curl -X GET http://localhost:8080/s3/list
```
### Download a File
```
curl -X GET http://localhost:8080/s3/download/sample.txt --output downloaded.txt
```
### Delete a File
```
curl -X DELETE http://localhost:8080/s3/delete/sample.txt
```
