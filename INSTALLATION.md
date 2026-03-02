#### Milvus images for Mac M1 processor
```bash
docker run -d --name milvus-standalone \
  --platform linux/amd64 \
  -p 19530:19530 \
  -p 9091:9091 \
  milvusdb/milvus:v2.2.12 \
  milvus run standalone
  ```


