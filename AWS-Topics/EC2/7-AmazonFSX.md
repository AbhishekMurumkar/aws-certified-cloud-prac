
* In case if you dont want to use EFS/S3, there is a third party - high performance file system on AWS
* fully managed service

## Amazon FSx for windows File server

* fully managed, highly reliable, scalable windows native shared file system
* applicable to use on windows ec2 instances, hence supports all windows protocol (SMB and windows NTFS)
* This is directly integrated with Microsoft Active Directory
* can be accessed from AWS or on-premise infrastructure

## Amazon FSx for lustre-->(Linux + cluster)

* this is used when you need a fully managed, scalable file storage for **High performance computing**(HPC)
* Usecases
  * machine learning
  * video processing
  * financial modelling
* scales up to 100GB/s, millions of IOPs, sub-ms latencies
* THis can be connected to your corporate data centers or through ec2 instances directly within in AWS 
* THis one directly stores data on S3 