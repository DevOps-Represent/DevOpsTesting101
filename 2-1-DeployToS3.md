# Deploy a static website to S3

### S3 = Amazon "Simple Storage Service"

***
## Key Concepts

S3 is a storage solution, designed to make web-scale computing easier for developers.

Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites.

Creating an S3 bucket is easy:
1. Create your account
2. Create a bucket
3. Add content to your bucket

https://docs.aws.amazon.com/s3/index.html

***
## 1. Create your bucket and set its permissions


### a. Access the S3 page
![s3homepage](images/2-1-S3/s3homepage.png)

#### Select "Create bucket"

### b. Fill in your bucket name and the region
![s3fillindetails](images/2-1-S3/s3nameregion.png)


### c. Confirm bucket creation
![s3createbucket](images/2-1-S3/s3createbucket.png)

### d. Static website hosting settings
![s3static](images/2-1-S3/s3staticwebsitehosting.png)

#### index.html
![s3index](images/2-1-S3/s3indexhtml.png)

### e. Set bucket policy
![s3bucketpolicy](images/2-1-S3/s3bucketpolicy.png)

Copy the below code to your bucket policy, and then edit the code with own bucket name in the 'example-bucket' text:

```
{
  "Version":"2012-10-17",
  "Statement":[{
	"Sid":"PublicReadGetObject",
        "Effect":"Allow",
	  "Principal": "*",
      "Action":["s3:GetObject"],
      "Resource":["arn:aws:s3:::example-bucket/*"
      ]
    }
  ]
}
```

## 2. Select and download a website template

### a. Select a website template you'd like to download

Go to this page for ready to go website templates: https://html5up.net/

(credit to the fantastic [AJ](https://twitter.com/ajlkn) for these templates)

### b. Download and unzip the website
![s3unzippedfiles](images/2-1-S3/s3extractedfiles.png)

## 3. Upload your website to your bucket

### a. Open the folder where your downloaded files are
![s3unzippedfiles](images/2-1-S3/s3extractedfiles.png)

### b. Upload the files

#### Select all
![s3selectall](images/2-1-S3/s3selectallfiles.png)


#### Drag these selected files and drop into S3

Ensure you include all the files, including the license and readme

![s3filesready](images/2-1-S3/s3readyforupload.png)

#### Upload
![s3filesready](images/2-1-S3/s3filesuploaded.png)

#### Ensure the index.html is visible in the bucket 'root' directory (not embedded in another folder)
![s3filesready](images/2-1-S3/s3checkindex.png)

## 3. Success! View your website
![s3homepage](images/2-1-S3/s3linktowebsite.png)

***

## Next steps - edit your website, or continue on with the agenda

### 1. Edit your website

#### Begin with the index.html file
1. Edit the file on your local machine using a text editor
2. Preview the changes in your browser
3. When you are happy with its look, upload the file again to S3

##### HTML tutorial:
https://www.w3schools.com/html/

### 2. Continue on with the agenda
https://github.com/DevOps-Girls/DevOpsTesting101/blob/master/1-0-Agenda.md
