# AWS Certified SysOps Administrator – Associate (Tips)

## General

- As per the AWS documentation for billing purposes, AWS treats all the accounts on the consolidated bill as if they were one account.

- When you work as a company with AWS, you will normally get an AWS representative. That representative will allow you carry out audits with third party vendors.

## VPC

- When you delete an instance the elastic network interface which in the below example of eth0 will also be deleted.

- You can expand your existing VPC by adding four (4) secondary IPv4 IP ranges (CIDRs) to your VPC.

- In AWS , when you try to delete a subnet which has instances it will not allow to delete it. 

- When you create a security group , by default all Outbound rules will be allowed.

- As per the AWS documentation it clearly mentions that the scaling process will be suspended if no instances launch in 24 hours.

## ENI

- You can create a secondary ENI that can be moved to a failover instance.

- You can assign a secondary private IP address to the primary ENI that can be moved to a failover instance.

## EC2

- You get charged for EC2 instances only when the instances are in a running state.

- The user can the set DisableApiTermination attribute to avoid accidental termination.

- You need to ensure you are entering the right user name if you get the error "Host key not found".

- The private key file has the wrong file permission if you get an Unprotected Private Key File error

- An instance reboot is equivalent to an operating system reboot.

- The user can disable the connection draining feature from EC2 -> ELB console or from CLI.

- Connection draining maximum timeout value can be just 3600 secs = 1 hour.

-  It is not possible to set the termination behavior to Stop for an Instance store backed AMI instance.

- If you want to launch Amazon Elastic Compute Cloud (EC2) Instances and assign each Instance a Predetermined private IP address you should launch the instances in the Amazon virtual Private Cloud (VPC).

## EBS

- A general EBS volume has a maximum IOPS of 3000, so even if you provision a volume of large size , it will not make a difference to the IOPS for the volume.

- As per the AWS documentation, by default, the EBS Snapshots limit is 10000.

- PIOPS does not support a size higher than 16384GiB.

- A placement group is a logical grouping of instances within a single Availability Zone. Placement groups are recommended for applications that benefit from low network latency, high network throughput, or both. To provide the lowest latency, and the highest packet-per-second network performance for your placement group, choose an instance type that supports enhanced networking.

- if you get the 'InsufficientInstanceCapacity' error that means AWS does not have sufficient capacity in that availability zone

## S3

- You can use the S3 storage analytics to see storage patterns.

- It is not possible to give access to an IAM user using ACL.

- Objects are directly accessible via a URL.

- The server side encryption with the user supplied key works when versioning is enabled.

- It is possible to have different encryption keys for different versions of the same object.

- If The user does not want to use the AES 256 encryption key provided by S3. then he should send the keys and encryption algorithm with each API call

- S3 allows you to store virtually unlimited amounts of data.

- You can set AWS bucket policy to make everything public

## AS

- Auto Scaling will throw an error since if there is a conflict in the schedule of two separate Auto Scaling Processes.

- If you suspend the terminate process, there is a chance that the instances can grow more than the maximum size due to AZRebalance.

- If the an instance becomes unhealthy as part of a health check then the instance is first terminated and then a new one is launched.
.
## ELB

- To ensure that a Classic Load Balancer stops sending requests to instances that are de-registering or unhealthy, while keeping the existing connections open, use connection draining.

- By default ELB will select the latest version of the policy

- The Connection draining time limit is set to 300.

-  SSL Protocols, SSL Ciphers and Server Order Preference are all part of the pre-defined policies.

- You can create a load balancer that uses the SSL/TLS protocol for encrypted connections (also known as SSL offload). This feature enables traffic encryption between your load balancer and the clients that initiate HTTPS sessions, and for connections between your load balancer and your EC2 instances.

## RDS

- The CNAME is changed to the standby DB when the primary one fails.

- The maximum retention period for automated backups are 35 days. All automated backups are deleted when you delete a DB instance. After you delete a DB instance, the automated backups can't be recovered.

- You can use Oracle GoldenGate with Amazon RDS for Active-Active database replication, zero-downtime migration and upgrades, disaster recovery, data protection, and in-region and cross-region replication.

- The patching or changes are first done to the standby instance. Once done, the standby will be promoted to the primary and then the patching is done on the primary.

- Read replicas can be created from a read replica of another read replica. 

- The maintenance window is only for scale operations or security patching.

- When you go to the Event dashboard in RDS, you can actually create event subscriptions based on Security groups.

- MultiAZ is supported for MySQL, MariaDb, Oracle and PostgreSQL. With Microsoft SQL server, you need to use the native mirroring to achieve High Availability.

- When you have an Event subscription, you can simply disable it by de-selecting on the Enabled option.

## IAM

- It is not possible to have the same login ID for multiple IAM users of the same account.

- IAM user can be a part of maximum 10 groups.

- One AWS account can have a maximum of 5000 IAM users.

- The organization can create 100 groups per AWS account.

- You can create an IAM policy with a condition which denies access when the IP address range is not from the organization.

- One AWS account can have 250 roles.

- Usernames can be a combination of up to 64 letters, digits, and these characters: plus (+), equal (=), comma (,), period (.), at sign (@), and hyphen (-). Names must be unique within an account. They are not distinguished by case.

-  A policy lets you specify the following:

   * Actions: what actions you will allow. Each AWS service has its own set of actions. For example, you might allow a user to use the Amazon S3 ListBucket action, which returns information about the items in a bucket. Any actions that you don't explicitly allow are denied.
   * Resources: which resources you allow the action on. For example, what specific Amazon S3 buckets will you allow the user to perform the ListBucket action on? Users cannot access any resources that you have not explicitly granted permissions to.
   * Effect: what the effect will be when the user requests access—either allow or deny. Because the default is that resources are denied to users, you typically specify that you will allow users access to resource.

## AWS Cloud formation

- The resources section is required by the CloudFormation template.

- You can customize your AWS deployments using JSON templates in CloudFormation.

- You can use a wait condition for situations like the following:

  * To coordinate stack resource creation with configuration actions that are external to the stack creation
  * To track the status of a configuration process

 ## CloudWatch
 
 - The user can set the alarm state to ‘Alarm’ using CLI to simulate alarms.
 
 - When your data is more sporadic and you have periods that have no associated data, you can choose to publish the value zero (0) for that period or no value at all. 
 
 - You can send cloudwatch metrics up to 2 hours in the future
 
 - Detailed monitoring is by default enabled for ELB for certain metrics with no additional charge.
 
 - The user can use the copy URL functionality of CloudWatch to share the exact details.
 
 - In command AWS cloudwatch put-metric-data  mandatory parameters for this command which is namespace and metricname URL.
 
 - Using the PutMetricData APIs the size of a request is limited to 8KB for HTTP GET requests and 40KB for HTTP POST requests.
 
 - As per AWS documentation when u enable Auto Scaling via CLI the detailed monitoring will be enabled.
 
 - When you create an ALARM, you have the option to add a notification as well. So the SNS service can be used to trigger a service which can then be used to trigger an instance in the private cloud.
 
 - The cloudwatch metrics for EMR is 5 minutes and cannot be configured beyond this.
 
 -  Ensure to go to Preferences in AWS and ensure that “Receive Billing Alerts” is enabled. Only then will you be able to define Clodwatch alarms on billing.
 
 - In the CloudWatch console you can select the local timezone under the Time Range tab to view the data as per the local timezone
 
 ## SQS
 
 - SQS messages does not guarantee the order of messages. So in order to do this, you need to add the sequencing information in each message itself.

- AWS reserve the right to delete a queue without notification if one of the following actions hasn't been performed on it for 30 consecutive days: SendMessage, ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission.

- As per the AWS documentation it clearly mentions that the default setting for message retention is 4 days.

- The SQS endpoint normally has the format of URL: https://sqs.AZ.amazonaws.com/ResourceID/Queuename.

## SNS

- SNS cannot provide data every minute.

## OpsWorks

- You can customize your AWS deployments using JSON templates in OpsWorks.

## Route 53

- The Dynamic Host Configuration Protocol (DHCP) provides a standard for passing configuration information to hosts on a TCP/IP network. The options field of a DHCP message contains the configuration parameters. 
