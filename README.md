# AWS Certified SysOps Administrator – Associate (Tips)

## General

- As per the AWS documentation for billing purposes, AWS treats all the accounts on the consolidated bill as if they were one account.

## VPC

- In AWS , when you try to delete a subnet which has instances it will not allow to delete it. 

- When you create a security group , by default all Outbound rules will be allowed.

- As per the AWS documentation it clearly mentions that the scaling process will be suspended if no instances launch in 24 hours.

## ENI

- You can create a secondary ENI that can be moved to a failover instance.

- You can assign a secondary private IP address to the primary ENI that can be moved to a failover instance.

## EC2

- You get charged for EC2 instances only when the instances are in a running state.

- You need to ensure you are entering the right user name if you get the error “Host key not found”.

- An instance reboot is equivalent to an operating system reboot.

- The user can disable the connection draining feature from EC2 -> ELB console or from CLI.

- Connection draining maximum timeout value can be just 3600 secs=1 hour.

- If you want to launch Amazon Elastic Compute Cloud (EC2) Instances and assign each Instance a Predetermined private IP address you should launch the instances in the Amazon virtual Private Cloud (VPC).

## EBS

- As per the AWS documentation, by default, the EBS Snapshots limit is 10000.

## S3

- You can use the S3 storage analytics to see storage patterns.

- Objects are directly accessible via a URL.

- S3 allows you to store virtually unlimited amounts of data.

- You can set AWS bucket policy to make everything public

## AS

= Auto Scaling will throw an error since if there is a conflict in the schedule of two separate Auto Scaling Processes.

## ELB

- To ensure that a Classic Load Balancer stops sending requests to instances that are de-registering or unhealthy, while keeping the existing connections open, use connection draining.

- The Connection draining time limit is set to 300.

-  SSL Protocols, SSL Ciphers and Server Order Preference are all part of the pre-defined policies.

## RDS

- The CNAME is changed to the standby DB when the primary one fails.

- When you go to the Event dashboard in RDS, you can actually create event subscriptions based on Security groups.


## IAM

- It is not possible to have the same login ID for multiple IAM users of the same account.

- You can create an IAM policy with a condition which denies access when the IP address range is not from the organization.

## AWS Cloud formation

- The resources section is required by the CloudFormation template.

- You can use a wait condition for situations like the following:

  * To coordinate stack resource creation with configuration actions that are external to the stack creation
  * To track the status of a configuration process

 ## CloudWatch
 
 - The user can set the alarm state to ‘Alarm’ using CLI to simulate alarms.
 
 -  The user can use the copy URL functionality of CloudWatch to share the exact details.
 
 - As per AWS documentation when u enable Auto Scaling via CLI the detailed monitoring will be enabled.
 
 - When you create an ALARM, you have the option to add a notification as well. So the SNS service can be used to trigger a service which can then be used to trigger an instance in the private cloud.
 
 -  Ensure to go to Preferences in AWS and ensure that “Receive Billing Alerts” is enabled. Only then will you be able to define Clodwatch alarms on billing.
 
 - In the CloudWatch console you can select the local timezone under the Time Range tab to view the data as per the local timezone
 
 ## SQS
 
 - SQS messages does not guarantee the order of messages. So in order to do this, you need to add the sequencing information in each message itself.

- As per the AWS documentation it clearly mentions that the default setting for message retention is 4 days.

- The SQS endpoint normally has the format of URL: https://sqs.AZ.amazonaws.com/ResourceID/Queuename.
