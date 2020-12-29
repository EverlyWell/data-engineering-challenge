# Data Engineering Challenge

### Overview

Using Python, we'd like you to create a process that allows us to store data being generated in one of our lab systems in our Data Warehouse.

* Spend no more than 4 hours on this, without counting initial setup or final documentation.

### Background

A laboratory is generating information in its own system. There are files that the laboratory produces in standard formats (`CSV` for this exercise) that record measurements from the instruments, along with patient information. In order to gather metrics and combine data from the lab with the rest of our application data, we would like to have the lab information stored in a Data Warehouse, where we can combine it with data from other sources.

### Requirements:

The application should fulfill the following requirements:

1. Include a README with description of your approach, and any other documentation you want to provide to describe your ETL process.
1. Data model (SQL schemas are best).
1. Code to process file and store the information in the Warehouse.

### Assumptions

* You can assume that the laboratory system will copy the files that the instruments generate to an S3 bucket, as your starting point.
* Files can arrive to S3 in a sequence that doesn't represent what happened in the real world. E.g. a file containing a result could arrive prior to a file containing the test taker information.
* One test taker can decide to take several tests (similar or different). Each test can have panel results for more than one analyte.
* Sample files have been provided in the [sample_data](./sample_data) directory for you to use as a guide.
* All new files that show up in S3 will contain all columns in the same order (no need to handle out-of-order headers).

### What We Like

* Resilient pipelines.
* Querying current data and historical data.
* Quality code.
* Being able to do automated QA.
