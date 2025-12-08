S3 style cloud blob storage providers.

From https://gist.github.com/Manouchehri/733e6235457e60de24fdbb15046fba7f (via https://news.ycombinator.com/item?id=38861711)

```
IDrive e2     - $0.005/GB  - $0 for download bandwidth - 1:3 upload:download ratio allowed <- questionable data privacy - custom domains offered - has audit logging - supports event notifications with AWS SQS - $0.01/GB overage on bandwidth - has replication
Backblaze B2  - $0.006/GB  - $0 for download bandwidth if through Worker (or $0.01/GB past a 1:3 upload:download ratio) <- decent data privacy record - no custom domains - has audit logging - has replication
Vultr         - $0.018/GB  - $0.01/GB for download <- https://www.vultr.com/products/object-storage/#pricing
Wasabi        - $0.0069/GB - $0 for download bandwidth - 1:1 and billed for 90 days <- has audit logging - no custom domains - min object size billed at 4 kilobytes
Storj         - $0.004/GB  - $0.007/GB for download <- not good for small files due to segment pricing
Scaleway      - $0.013/GB  - $0.011/GB for download <- estimate, had to do EUR to USD conversion https://www.scaleway.com/en/pricing/storage/
Cloudflare R2 - $0.015/GB  - $0.00/GB for download, $4.50 / million for uploads and $0.36 / million for downloads requests 
DigitalOcean  - $0.020/GB  - $0.01/GB for download
Google GCS    - $0.020/GB  - $0.08/GB for download (best case) <- https://cloud.google.com/storage/pricing#network-egress
IBM Storage   - $0.0209/GB - $0.05/GB for download (best case) <- https://cloud.ibm.com/objectstorage/create#pricing
Amazon AWS S3 - $0.021/GB  - $0.05/GB for download (best case) <- https://aws.amazon.com/s3/pricing/
Oracle Cloud  - $0.0255/GB - $0.0085/GB for download, $0 for download bandwidth if through Worker <- https://www.oracle.com/cloud/storage/pricing/
Alibaba Cloud - $0.0173/GB - $0.094/GB for download (best case during peak), assuming Beijing <- https://www.alibabacloud.com/en/product/oss/pricing?_p_lc=1#tab1-1
Akamai Linode - $0.02/GB   - $0.005/GB for download
OVH Object    - $0.008/GB  - $0.011/GB for download
Hetzner       - $0.0053/GB - $0.00106/GB for download after 1:1 ratio <- estimate, had to do EUR to USD conversion - min object size billed at 64 kilobytes
Telnyx Cloud  - $0.023/GB  - $0.00/GB for download - does not supported presigned URLs due to crazy bad auth design choice <- https://telnyx.com/the-better-amazon-s3-alternative
```

%%
TODO: parse this table and do a visualization.
%%
