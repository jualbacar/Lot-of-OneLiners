# Lot-of-OneLiners
Oneliners everywhere


+ AWS
  - Get Bucket Size
  
    ```aws s3 ls s3://bucket_name --recursive | grep -v -E "(Bucket: |Prefix: |LastWriteTime|^$|--)" | awk 'BEGIN {total=0}{total+=$3}END{print total/1024/1024/1024" GB"}'```
+ Apache
  - Top 10 requests per IP and User-Agent
  
    ``` hello ```
