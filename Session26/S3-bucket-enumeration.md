# S3 Bucket Enumeration  

1. clone lazys3 
   
   ```
   git clone https://github.com/nahamsec/lazys3.git
   ```
   
   ```
   ruby lazys3.rb  company-name
   ```

2. Using s3scanner

   ```sh
   mkdir s3
   python -m venv s3scan
   source s3scan/bin/activate
   pip install --upgrade pip
   pip install s3scanner
   ```
   ```
   python -m S3Scanner scan --bucket  URL
   ```
   ```
   python -m S3Scanner dump --bucket URL --dump-dir ~/dir1
   ```
   ```
   python -m S3Scanner scan --threads 10 --bucket  URL
   ```

## Another Scanner 
   
   ```
   git clone https://github.com/GermanAizek/S3-Bucket-Scanner.git
   cd S3-Bucket-Scanner
   pip install -r requirements.txt
   ```   

   ```
   python3 s3scanner.py bucket-name
   ```
   ```
   python3 s3scanner.py -l bucket-name
   ```
   ```
   python3 s3scanner.py bucket-list-filename
   ```
   ```
   python3 s3scanner.py bucket-name --dump
   ```

3. using AWS CLI

Install AWS CLI v2 on Kali Linux

```
curl -fsSL "https://awscli.amazonaws.com/v2/install.sh" | bash
```

Verify with `aws --version`

```
aws s3 ls s3://bucket-name --no-sign-request
```

```
aws s3 cp s3://bucket-name/file.txt  ~/files/ --no-sign-request
```

```
aws s3api get-bucket-acl --bucket-name --no-sign-request
```

```
aws s3api put-bucket-acl --bucket bucket-name --grant-full-control emailaddress=youremail-id
```

```
aws s3api get-bucket-versioning --bucket bucket-name --no-sign-request
```

