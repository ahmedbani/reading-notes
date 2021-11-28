# S3


### **Amazon S3**
+ ***Advantages of using Amazon S3:***
Amazon S3 is intentionally built with a minimal feature set that focuses on simplicity and robustness. Following are some of the advantages of using Amazon S3:

    + Creating buckets – Create and name a bucket that stores data. Buckets are the fundamental containers in Amazon S3 for data storage.

    + Storing data – Store an infinite amount of data in a bucket. Upload as many objects as you like into an Amazon S3 bucket. Each object can contain up to 5 TB of data. Each object is stored and retrieved using a unique developer-assigned key.

    + Downloading data – Download your data or enable others to do so. Download your data anytime you like, or allow others to do the same.

    + Permissions – Grant or deny access to others who want to upload or download data into your Amazon S3 bucket. Grant upload and download permissions to three types of users. Authentication mechanisms can help keep data secure from unauthorized access.

    + Standard interfaces – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.

+ ***Buckets:***
Buckets serve several purposes:
    + They organize the Amazon S3 namespace at the highest level.

    + They identify the account responsible for storage and data transfer charges.

    + They play a role in access control.

    + hey serve as the unit of aggregation for usage reporting.

+ ***Objects:***
Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata. The data portion is opaque to Amazon S3. The metadata is a set of name-value pairs that describe the object. These include some default metadata, such as the date last modified, and standard HTTP metadata, such as Content-Type. You can also specify custom metadata at the time the object is stored.

+ ***Keys:***
A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key. The combination of a bucket, key, and version ID uniquely identify each object.

#### **Amazon S3 features**
This section describes important Amazon S3 features:
+ Storage classes
+ Bucket policies
+ AWS Identity and Access Management
+ Access control lists
+ Versioning
+ Operations

+ **resources:** 

    *[https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)*


[Home Page](../README.md)
