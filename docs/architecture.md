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



Some important notes
* Many of the technologies overlap the abobe areas of concern, and will be mentioned multiple times based on thier utilization. 
* This analysis is purely techincal and has not factored in cost, which will be critical when making implementation decisions.
* While all technologies are in the cloud, some are (from the consumers perspective) purely serverless, while others require you to provision virtual machines 


# Solution

The solution would include the following Amazon technologies


# Utilization




# Research

## General
Amazon has realized the 
### Glue



### Lake Formation
Lake formation is still in a preview release, but is scheduled to be public within the next quarter.



## Storage

The one common denominator of all potential AWS solutions is the utilization of S3 as a general storage layer

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




## Security

The initial concern is to prevent unauthorized access from any outside sources



### Identity Access Management (IAM)

 

 

### S3

## Processing

### Glue

### Lambda

### EMR




``` 
Resources 
 [Data Pipelines w/ Glue](https://www.youtube.com/watch?v=6tBp2JuYmSg)
```

## Platform Monitoring and Auditing


> Resources 
> * [Glue Monitoring](https://docs.aws.amazon.com/glue/latest/dg/monitor-glue.html)
