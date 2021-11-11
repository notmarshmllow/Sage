# Sage - Fast Scraping Tool to quickly find S3 Buckets, S3 Bucket Takeover and URLs from organization's GitHub Repositories.

![alt_text](https://github.com/notmarshmllow/Sage/blob/main/sample-image.png)

# INSTALLATION

Requirement: Python: 3.7+

```
git clone https://github.com/notmarshmllow/sage.git
cd Sage
pip install -r requirements.txt
python3 sage.py -h
```

# USAGE
Sage takes the name of the organization and tries to find all S3 Buckets in the Orgnization's GitHub Repositories.

Following usage example show simplest tasks you can acomplish with `Sage`.

# CREDENTIALS

Please update you GitHub Login credentials in `cred.py` file.
Make sure you do not have two-factor authentication (2FA) turned ON. This may cause issues for tool to run.

Credentials are required to use the tool or else the tool will not run.

# ORGANIZATION'S NAME

The `-org` switch takes the Organization's name and finds all the S3 Buckets associated with the Organization in the Organization's Repository.

```
python3 sage.py -org Google
```

# NUMBER OF PAGES TO SCRAPE

The `-p` switch takes integer as input. It accepts the number of pages to scrape (default: 100)

```
python3 sage.py -org Google -p 8
```

# CUSTOM QUERY

The `-q` switch can be used to search for custom query. By default, sage looks for 's3.amazonaws.com' to find s3 Buckets.

```
python3 sage.py -org Google -q us-west
```

# FINDING SUBDOMAINS

The `-q` switch can also be used to find Subdomains of a domain.

```
python3 sage.py -org Apple -q apple.com
```

Note: Output will only be URLs and not any other String.

Be Creative with this!


# OUTPUT TO A FILE

The `-o` switch prints output to a file.

```
python3 sage.py -org Google -p 8 -o google_s3.txt
```

# S3 Bucket Takoover

Sage finds all the S3 Buckets of an organization and also finds out any unclaimed Buckets.

If a bucket is vulnerable, Sage display that the Takeover of the Bucket is possible.


#  EXCLUDE

If you find any repetative or irreleant bucket that isn't associated with your target but still is being scrapped, you can include it in the `exclude=[]` list in `sage.py` file. This will make sure that the bucket name isn't shown in the Output anymore.




All developments to Sage are highly welcomed and much appreciated!

Sage - Developed by [@notmarshmllow](https://twitter.com/notmarshmllow):heart:
