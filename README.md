# Lot-of-OneLiners
Oneliners everywhere


+ AWS
  - Get Bucket Size
  
    ```aws s3 ls s3://bucket_name --recursive | grep -v -E "(Bucket: |Prefix: |LastWriteTime|^$|--)" | awk 'BEGIN {total=0}{total+=$3}END{print total/1024/1024/1024" GB"}'```
+ Apache
  - Top 10 requests per IP and User-Agent
  
    ```cat log_file.log | sed -e 's/^\([[:digit:]\.]*\).*"\(.*\)"$/\1 \2/' | sort -n | uniq -c | sort -hr | head -10```
    
  - Top 10 requests por IP
  
    ```awk -F\" '{print $1}' log_file.log | sort | uniq -c | sort -hr | head -10```
    
  - Top 10 requests per User-Agent
  
    ```awk -F\" '{print $6}' log_file.log | sort | uniq -c | sort -hr | head -10```
