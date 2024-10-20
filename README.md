# AWS Certified SysOps Administrator – Associate (Tips)
* AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS. Using AWS Direct Connect, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections.
* You can create three types of Amazon Route 53 health checks:
  * Health checks that monitor an endpoint.
  * Health checks that monitor other health checks (calculated health checks).
  * Health checks that monitor CloudWatch alarms.
* PercentIOLimit – Shows how close a file system is to reaching the I/O limit of the General Purpose performance mode. If this metric is at 100 percent more often than not, consider moving your application to a file system using the Max I/O performance mode.
* ACM provides managed renewal for your Amazon-issued SSL/TLS certificates. This means that ACM will either renew your certificates automatically (if you are using DNS validation), or it will send you email notices when expiration is approaching. These services are provided for both public and private ACM certificates.
* Having a single login URL for different AWS accounts is not possible.
* If you want to remediate non-compliant security groups, you can do so using AWS Systems Manager Automation documents. These documents define the actions to be performed on noncompliant AWS resources evaluated by AWS Config Rules.
* You can improve performance by increasing the proportion of your viewer requests that are served from CloudFront edge caches instead of going to your origin servers for content; that is, by improving the cache hit ratio for your distribution. This can be done by doing any of the following:
  * Increase the TTL of your objects
  * Configure the distribution to forward only the required query string parameters, cookies, or request headers for which your origin will return unique objects.
  * Remove Accept-Encoding header when compression is not needed
  * Serving Media Content by using HTTP
* AWS Backup follows the default mechanism of taking backups. In this case, the default mechanism for backing up EBS volumes is to backup with no-reboot behavior. This means that AWS Backup will not be able to help you create an AMI that guarantees file system integrity since you need to reboot the instance to do this.
* A resource is considered to have drifted if any of its actual property values differ from the expected property values. This includes if the property or resource has been deleted. To determine the configured changes in the resources, you can use drift detection. Drift detection enables you to detect whether a stack’s actual configuration differs, or has drifted, from its expected configuration. Resolving drift helps to ensure configuration consistency and successful stack operations.
* Oracle database on a RAC configuration is not supported by RDS.
* A NAT instance/gateway does not support IPv6 address. You have to use an egress-only Internet gateway instead.
* Associate the CreationPolicy attribute with a resource to prevent its status from reaching create complete until AWS CloudFormation receives a specified number of success signals or the timeout period is exceeded.
* Access logging is an optional feature of Elastic Load Balancing that is disabled by default. After you enable access logging for your application load balancer, Elastic Load Balancing captures the logs and stores them in the Amazon S3 bucket that you specify as compressed files.
* AWS Systems Manager Run Command lets you remotely and securely manage the configuration of your managed instances.
* AWS Storage Gateway connects an on-premises software appliance with cloud-based storage to provide seamless integration with data security features between your on-premises IT environment and the AWS storage infrastructure.
* You can configure your AWS account to enforce the encryption of the new EBS volumes and snapshot copies that you create.
* The WaitOnResourceSignals property specifies whether the Auto Scaling group waits on signals from new instances during an update. Use this property to ensure that instances have completed installing and configuring applications before the Auto Scaling group update proceeds. AWS CloudFormation suspends the update of an Auto Scaling group after new EC2 instances are launched into the group. AWS CloudFormation must receive a signal from each new instance within the specified PauseTime before continuing the update.
* When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload.
* To enable instances in your VPC to reach your customer gateway, you must configure your route table to include the routes used by your VPN connection and point them to your virtual private gateway.
* You can use the existing Parameters section of your CloudFormation template to define Systems Manager parameters, along with other parameters. Systems Manager parameters are a unique type that is different from existing parameters because they refer to actual values in the Parameter Store. The value for this type of parameter would be the Systems Manager (SSM) parameter key instead of a string or other value. CloudFormation will fetch values stored against these keys in Systems Manager in your account and use them for the current stack operation.
* Your launch template determines all the possible Spot capacity pools (instance types and Availability Zones) from which Spot Fleet can launch Spot Instances. However, when launching instances, Spot Fleet uses the allocation strategy that you specify to pick the specific pools from all your possible pools. You can specify one of the following allocation strategies:
  * - priceCapacityOptimized
  * - capacityOptimized
  * - diversified
  * - lowestPrice
  * - InstancePoolsToUseCount
* RI discounts apply to accounts in an organization’s consolidated billing family depending upon whether RI sharing is turned on or off for the accounts. By default, RI sharing for all accounts in an organization is turned on. The management account of an organization can change this setting by turning off RI sharing for an account.
* Amazon S3 inventory is one of the tools Amazon S3 provides to help manage your storage. You can use it to audit and report on the replication and encryption status of your objects for business, compliance, and regulatory needs.
* In a Multi-AZ deployment, Amazon FSx automatically provisions and maintains a standby file server in a different Availability Zone.
* Since tags are case-sensitive, giving them a consistent naming format is a good practice. Depending on how your tagging rules are set up, having a disorganized naming convention may lead to permission issues like the one described in the scenario. In the scenario, the administrator can leverage the require-tags managed rule in AWS Config. This rule checks if a resource contains the tags that you specify.
* As your infrastructure grows, common patterns can emerge in which you declare the same components in multiple templates. You can separate out these common components and create dedicated templates for them. Then use the resource in your template to reference other templates, creating nested stacks.
* With RAID 0, I/O is distributed across the volumes in a stripe. If you add a volume, you get the straight addition of throughput and IOPS. The resulting size of a RAID 0 array is the sum of the sizes of the volumes within it, and the bandwidth is the sum of the available bandwidth of the volumes within it. For example, two 500 GiB io1 volumes with 4,000 provisioned IOPS each create a 1000 GiB RAID 0 array with an available bandwidth of 8,000 IOPS and 1,000 MiB/s of throughput.
* 
