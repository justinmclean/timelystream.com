---
layout: docu
title: S3 Import
selected: S3 Parquet Import
---

## How to load a Parquet file directly from S3

To load a Parquet file from S3, the `HTTPFS` extension is required. This can be installed use the `INSTALL` SQL command. This only needs to be run once.

```sql
INSTALL httpfs;
```

To load the `HTTPFS` extension for usage, use the `LOAD` SQL command:

```sql
LOAD httpfs;
```

After loading the `HTTPFS` extension, set up the credentials and S3 region to read data. You may either use an access key and secret, or a token.

```sql
SET s3_region='us-east-1';
SET s3_access_key_id='<AWS access key id>';
SET s3_secret_access_key='<AWS secret access key>';
```
The alternative is to use a token:
```sql
SET s3_region='us-east-1';
SET s3_session_token='<AWS session token>';
```

After the `HTTPFS` extension is set up and the S3 credentials are correctly configured, Parquet files can be read from S3 using the following command:

```sql
SELECT * FROM read_parquet('s3://<bucket>/<file>');
```
