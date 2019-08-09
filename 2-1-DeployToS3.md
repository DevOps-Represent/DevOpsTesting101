# Deploy a static website to S3

### S3 = Amazon "Simple Storage Service"

***
## Key Concepts

It is designed to make web-scale computing easier for developers.

Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites.

Creating an S3 bucket is easy:
1. Create your account
2. Create a bucket
3. Add content to your bucket

https://docs.aws.amazon.com/s3/index.html

***
## 1. Create your bucket and set its permissions

### a. Access the S3 page

### b. Fill in your bucket name and the region

### c. Confirm bucket creation

### d. Static website hosting settings

#### index.html

### e. Set bucket policy

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

### b. Download and unzip the website


## 3. Upload your website to your bucket

### a. Open the folder where your downloaded files are

### b. Upload the files

#### Select all


#### Drag and drop


#### Ensure the index.html is visible in the bucket 'root' directory (not embedded in another folder)

## 3. Success! View your website

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
