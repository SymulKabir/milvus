#### Milvus images for Mac M1 processor
```bash
curl -o docker-compose.yml https://raw.githubusercontent.com/milvus-io/milvus/master/deployments/docker/standalone/docker-compose.yml


docker compose up -d
  ```
**Find where the data is stored**

Run:
```bash
docker inspect milvus-minio | grep Source
docker inspect milvus-etcd | grep Source
docker inspect milvus-standalone | grep Source
```
You will see something like:
```bash
"Source": "/path/to/minio_data"
"Source": "/path/to/etcd_data"
"Source": "/path/to/milvus_data"
```
These three folders are your actual Milvus database.





