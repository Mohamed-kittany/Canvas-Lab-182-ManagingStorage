# Managing Storage

## Lab Overview

This project focuses on managing data on Amazon Elastic Block Store (Amazon EBS) volumes using various AWS services and tools. The tasks include creating and managing snapshots of EBS volumes, automating snapshot deletion, and syncing data to Amazon Simple Storage Service (Amazon S3). Additionally, Amazon S3 versioning is utilized to retrieve deleted files.

<img width="769" alt="architecture" src="https://github.com/Mohamed-kittany/Canvas-Lab-183-ManagingStorage/assets/161580792/5c30b044-fed8-44f1-b505-7317ea9e1c2f">

## Tasks Completed

### 1. Creating and Maintaining Snapshots for Amazon EC2 Instances

- **Created EBS Snapshots**:
  - Utilized the AWS CLI to create snapshots of an EBS volume attached to the "Processor" instance.
  - Verified the creation of snapshots in the AWS Management Console.

- **Automated Snapshot Deletion**:
  - Developed Python scripts to identify and delete older snapshots based on predefined criteria.
  - Configured a scheduler (using cron) on the "Command Host" instance to run the Python scripts periodically, ensuring automated maintenance of EBS snapshots.

### 2. Syncing Data from EBS Volume to Amazon S3

- **Installed AWS CLI**:
  - Set up the AWS CLI on the "Command Host" instance to enable command-line management of AWS resources.

- **Synced EBS Volume Data to S3**:
  - Executed the `aws s3 sync` command to sync the contents of a directory on the "Processor" instance's EBS volume to an S3 bucket.
  - Verified the successful synchronization by checking the files in the S3 bucket.

### 3. Using Amazon S3 Versioning to Retrieve Deleted Files

- **Enabled S3 Versioning**:
  - Enabled versioning on the designated S3 bucket to maintain multiple versions of objects and facilitate file recovery.

- **Retrieved Deleted Files**:
  - Tested the versioning feature by deleting a file and retrieving its previous version from the S3 bucket, ensuring data integrity and recoverability.

### Challenge

- **S3 Sync Command**:
  - Successfully synced the contents of a directory on an EBS volume to an S3 bucket using the `aws s3 sync` command, demonstrating proficiency in data management and transfer within the AWS ecosystem.

## Conclusion

Throughout this project, I gained hands-on experience in managing EBS snapshots, automating maintenance tasks with Python scripts, and utilizing AWS CLI for data synchronization. Additionally, I explored the use of Amazon S3 versioning to ensure data durability and accessibility, reinforcing best practices in cloud storage management.

