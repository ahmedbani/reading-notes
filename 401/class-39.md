# Amazon Kinesis

- **What is Amazon Kinesis?**
    - *Amazon Kinesis is a fully managed service for real-time processing of streaming data at massive scale. Amazon Kinesis can collect and process hundreds of terabytes of data per hour from hundreds of thousands of sources, so you can write applications that process information in real-time.* 

    - With Amazon Kinesis applications, we can build real-time dashboards, capture exceptions and generate alerts, drive recommendations, and make other real-time business or operational decisions. We can also easily send data to other services such as Amazon Simple Storage Service, Amazon DynamoDB, and Amazon Redshift.

    - The two classes `AWSKinesisRecorder` and `AWSFirehoseRecorder` allow us to interface with Amazon Kinesis and Amazon Kinesis Firehose to stream analytics data for real-time processing.

### What is Amazon Kinesis Firehose?

- Amazon Kinesis Firehose is a fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3) and Amazon Redshift. 
- With Firehose, we do not need to write any applications or manage any resources. we configure our data producers to send data to Firehose and it automatically delivers the data to the destination that we specified.
- The Amazon Kinesis Firehose AWSFirehoseRecorder client lets us store PutRecords requests on disk and then send them using Kinesis Data FirehosePutRecordBatch.

> Integrating Amazon Kinesis
- `aws-android-sdk-kinesis` library enables sending analytics to Amazon Kinesis.
- `aws-android-sdk-mobile-client` library gives access to the AWS credentials provider and configurations.

### Resources
- [Amplify and Kinesis](https://docs.amplify.aws/sdk/analytics/kinesis/q/platform/android/#working-with-the-api)