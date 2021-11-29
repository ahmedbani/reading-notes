# Notifications


### **SNS with Amplify (and Firebase):**

#### **Setting up access for Amazon SNS:**
+ Step 1: Create an AWS account and an IAM administrator user.
+ Step 2: Create an IAM user and get your AWS credentials


#### **Getting started with Amazon SNS:**
+ Step 1: Create a topic.
+ Step 2: Create a subscription to the topic.
+ Step 3: Publish a message to the topic.
+ Step 4: Delete the subscription and topic.


#### **Publish Amazon SNS Messages Privately:**
Implement a fanout messaging scenario using Amazon Simple Notification Service (SNS)and Amazon Simple Queue Service (SQS). In this scenario, messages are "pushed" tomultiple subscribers, which eliminates the need to periodically check or poll forupdates and enables parallel asynchronous processing of the message by thesubscribers.


#### **Publish Amazon SNS Messages Privately:**
In some cases, your applications may require higher levels of security and need to be deployed into a private network. Some common cases for private networking and messaging include:

+ Isolating development and testing environments
+ Sharing personally identifiable information (PII) about your customers
+ Hosting a PCI-compliant e-commerce website
+ Developing healthcare applications subject to HIPAA
+ Implementing a cryptographic algorithm subject to FIPS 140
+ Processing mortgage applications in a banking system

#### **Filter Messages Published to Topics**
We will use a fanout messaging pattern using SNS and SQS to decouple the website from the backend systems. To get the event notifications to the right backend system, you could create a separate topic for each type of quote request, then add message routing logic to your publisher. However, this option can result in overly complicated publishers, topic proliferation, and additional overhead in provisioning and managing your SNS topics. SNS message filtering is much simpler!


+ **resources:** 

    *[https://aws.amazon.com/sns/getting-started/](https://aws.amazon.com/sns/getting-started/)*


