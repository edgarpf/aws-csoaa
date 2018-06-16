# AWS Certified SysOps Administrator – Associate (Tips)

## ENI

- You can create a secondary ENI that can be moved to a failover instance.

- You can assign a secondary private IP address to the primary ENI that can be moved to a failover instance.

## EC2

- You get charged for EC2 instances only when the instances are in a running state.

- The user can disable the connection draining feature from EC2 -> ELB console or from CLI.

- If you want to launch Amazon Elastic Compute Cloud (EC2) Instances and assign each Instance a Predetermined private IP address you should launch the instances in the Amazon virtual Private Cloud (VPC).

## EBS

- As per the AWS documentation, by default, the EBS Snapshots limit is 10000.

## S3

- You can use the S3 storage analytics to see storage patterns.

- Objects are directly accessible via a URL.

- S3 allows you to store virtually unlimited amounts of data.

- You can set AWS bucket policy to make everything public

## ELB

- The Connection draining time limit is set to 300.

-  SSL Protocols, SSL Ciphers and Server Order Preference are all part of the pre-defined policies.

## RDS

- The CNAME is changed to the standby DB when the primary one fails.

## IAM

- It is not possible to have the same login ID for multiple IAM users of the same account.

## AWS Cloud formation

- The resources section is required by the CloudFormation template.

 ## CloudWatch
 
 - The user can set the alarm state to ‘Alarm’ using CLI to simulate alarms.
 
 -  Ensure to go to Preferences in AWS and ensure that “Receive Billing Alerts” is enabled. Only then will you be able to define Clodwatch alarms on billing.
 
 - In the CloudWatch console you can select the local timezone under the Time Range tab to view the data as per the local timezone
 
 ## SQS
 
 - SQS messages does not guarantee the order of messages. So in order to do this, you need to add the sequencing information in each message itself.
