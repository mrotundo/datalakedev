# Data Lake Architecture


* [Overview](#overview)
* [Soluition](#solution)
* [Utilization](#utilization)
* [Research](#research)



# Overview

The Amazon services offering is rapidly evolving and that is exceptionally true of the big data / anayltics space. What is detailed in this document is a best approach at a general purpose data lake solution for a large enterprise. 

## Solution Areas of Concern

* Storage
* Security
* Data Processing
* Data Ingestion
* Data Management
* Process Management
* Backup and Redundancy
* System Monitoring and Auditing
* Machine Learning 

## Implementation


The implementation of technical components of the cloud solution can be broken down into three general buckets:
* **Cloud Native** - Service offered by the cloud provider that requires zero provisioning or installation. It is entirely a managed service that only requires the configuration
* **Cloud Provisioned** - Service offered by the cloud provider that requires virtual hardware be provisioned/scaled directly by end-user to allow for its functioning.
* **Cloud Hosted** - A third party or open source technology that is hosted on the cloud, but must be maintained by the end user. This would also require that the virtual hardware be provisioned by the end user.

The ideal solution is entirely cloud native because of 
Although the inherent risk of pure cloud native doing so is that you are entirely dependent on this provider. If the services drastically change or costs become untenable, migrating out 



It is important to note that due to time constraints this analysis does not factor in cost. 


# Solution

The solution would include the following Amazon technologies:
* API Gateway
* EMR
* Glue
* Lake Formation
* Lambda
* Kineisis
* Redshift
* Redshift Spectrum
* S3

## Core Functionality
Amazon has two overlapping technologies that focus on providing Data Lake functionality and management capabilities, (Glue)[#glue] and (Lake Formation)[#lake-formation]. Glue focuses on ETL, but also provides data catalog functionality with tools to automate its upkeep.    

For storage (S3)[#s3] is 




# Utilization
## 
## Basic Data Processing / ETL
Apache Glue utilizes

## Complex Processing


## Machine Learning
More research required

# Research

## General
Amazon has realized the 
### Glue



### Lake Formation
Lake formation is still in a preview release, but is scheduled to be public within the next quarter.


**Resources**
* [Lake Formation Tech Talk](https://www.youtube.com/watch?v=nsiLMqg654s)

## Storage

The one common denominator of all potential AWS solutions is the utilization of S3 as a general storage layer

### S3


### Redshift
Redshift is a columnar store offering from Amazon.


### Redshift Spectrum
Redshift Spectrum extends the capabilities of Redshift beyond the 

### Athena
While Athena is not a storage technology, it can act as a replacement for Redshift Spectrum (or other columnar store tech) by allowing for this querying behavior directly off of S3.

### Glacier
Glacier is fundamentally S3

> Resources 
> * [Redshift Spectrum vs Athena](https://blog.openbridge.com/how-is-aws-redshift-spectrum-different-than-aws-athena-9baa2566034b)
> * [Athena Review](https://www.youtube.com/watch?v=gGJ4zxeG9PI)





## Security

The initial concern is to prevent unauthorized access from any outside sources

### Identity Access Management (IAM)




## Processing

### Glue
Glue itself utilizes a limited version of Spark to handle job processing. Currently it only supports Scala and Python.

### Lambda
General purpose serverless processing 

### EMR


## Process Management

### Glue




**Resources** 
* [Data Pipelines w/ Glue](https://www.youtube.com/watch?v=6tBp2JuYmSg)
* [Glue vs Lambda for ETL](https://www.reddit.com/r/aws/comments/9umxv1/aws_glue_vs_lambda_costbenefit/)


## Platform Monitoring and Auditing

### CloudWatch

**Resources** 
* [Glue Monitoring](https://docs.aws.amazon.com/glue/latest/dg/monitor-glue.html)
