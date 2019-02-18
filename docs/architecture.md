# Data Lake Architecture


* Overview



## Overview

The Amazon services offering is rapidly evolving and that is exceptionally true of the big data / anayltics space. What is detailed in this document is a best approach at a general purpose data lake solution for a large enterprise. 

* General
* Storage
* Security
* Data Processing
* Transfer
* Data Management
* Process Management


Some important notes
* Many of the technologies overlap the abobe areas of concern, and will be mentioned multiple times based on thier utilization. 
* This analysis is purely techincal and has not factored in cost, which will be critical when making implementation decisions.
* While all technologies are in the cloud, some are (from the consumers perspective) purely serverless, while others require you to provision virtual machines 

## General
Amazon has realized the 
### Glue



### Lake Formation
Lake formation is still in a preview release, but is scheduled to be public within the next quarter.



## Storage



The one common denominator of all potential AWS solutions is the utilization of S3 as a general storage layer

### Redshift


### Redshift Spectrum

### Athena
While Athena is not a storage technology, it can act as a replacement for Redshift Spectrum (or other columnar store tech) by allowing for this querying behavior directly off of S3.

## Security

The initial concern is to prevent unauthorized access from any outside sources



### Identity Access Management (IAM)

 

 https://docs.aws.amazon.com/aws-technical-content/latest/building-data-lakes/securing-protecting-managing-data.html

### S3

## Processing

### Glue

Resources 
* [Data Pipelines w/ Glue](https://www.youtube.com/watch?v=6tBp2JuYmSg)