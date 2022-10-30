# <center>Elastic File System</center>

Managed NFS --Shared NFD that can be mounted on 100's of EC2 instances at a time

Works only with Linux 

Highly available, scalable, expensive, pay per use 

| <center>EBS</center> | <center>EFS</center> |
| --- | --- |
| can be attached to one specific in one AZ. For moving we need to create a snapshot and share the same snapshot across different AZ| Since this is shared FS we dont have to do anything for sake of sharing, **you just have to mount to same mount point on all instances to have all shared data** |

## EFS Infrequent Access (EFS-IA)

This stoage is cost optimized, which is used mostly to store the files that are least accessed (60% cost lowered than EFS).
In this storage, the files whose last accessed date are more than 60days will be moved into EFS-IA automaticaly, if you enable this. We can enable this via **Lifecycle Policy**