# EC2

#### Amazon EC2 (Elastic Compute Cloud) Detailed Notes

Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud. Using Amazon EC2 eliminates the need to invest in hardware upfront, allowing you to develop and deploy applications faster. Below is a detailed breakdown covering all aspects of EC2, including instances, AMIs, EBS, Security Groups, and Auto Scaling.

***

**EC2 Instances**

1. **Instance Types**
   * **General Purpose**: Balanced compute, memory, and networking (e.g., T3, T3a, M5, M6g).
   * **Compute Optimized**: High-performance processors for compute-intensive applications (e.g., C5, C6g).
   * **Memory Optimized**: For memory-intensive applications (e.g., R5, X1, X2gd).
   * **Storage Optimized**: High, sequential read/write access to large datasets on local storage (e.g., I3, I3en).
   * **Accelerated Computing**: Use of GPU or FPGA for high-performance computing (e.g., P3, G4, F1).
2. **Instance Lifecycle**
   * **Launch**: Start an instance from an AMI.
   * **Stop/Start**: Instances can be stopped and restarted without losing data stored on EBS volumes.
   * **Terminate**: Permanently delete an instance.
   * **Reboot**: Restarts the instance but does not change its state.
3. **Billing and Pricing**
   * **On-Demand**: Pay for compute capacity by the second or hour.
   * **Reserved Instances**: Significant discount (up to 75%) over On-Demand pricing.
   * **Spot Instances**: Up to 90% discount over On-Demand prices but can be interrupted.
   * **Savings Plans**: Flexible pricing model with significant savings.
4. **Networking**
   * **Elastic Network Interfaces (ENIs)**: Virtual network cards attached to EC2 instances.
   * **Public and Private IP Addresses**: Instances can have both for public internet and private network communication.
   * **Elastic IP Addresses**: Static public IP addresses for dynamic cloud computing.
   * **Enhanced Networking**: High throughput and low-latency for network-intensive applications (e.g., ENA, SR-IOV).

***

**Amazon Machine Images (AMIs)**

1. **AMI Components**
   * **Root Volume Template**: Specifies the root volume for the instance (OS, application server, applications).
   * **Launch Permissions**: Controls which AWS accounts can use the AMI to launch instances.
   * **Block Device Mapping**: Specifies the volumes to attach to the instance at launch.
2. **Types of AMIs**
   * **EBS-Backed AMIs**: Root device for an instance launched from the AMI is an Amazon EBS volume.
   * **Instance Store-Backed AMIs**: Root device for an instance launched from the AMI is an instance store volume.
3. **Creating and Using AMIs**
   * **Creating an AMI**: Create custom AMIs from existing EC2 instances.
   * **Sharing AMIs**: Share AMIs with specific AWS accounts or make them public.
   * **Cross-Region AMI Copy**: Copy AMIs to other regions.
4. **Managing AMIs**
   * **Registration**: Registering the AMI with EC2.
   * **Deregistration**: Unregistering an AMI when no longer needed.
   * **Lifecycle**: Maintain AMI versions for different stages of development.

***

**Elastic Block Store (EBS)**

1. **EBS Volume Types**
   * **General Purpose SSD (gp2, gp3)**: Balanced price and performance.
   * **Provisioned IOPS SSD (io1, io2)**: High-performance storage for critical workloads.
   * **Throughput Optimized HDD (st1)**: Low-cost HDD for frequently accessed, throughput-intensive workloads.
   * **Cold HDD (sc1)**: Lowest cost HDD designed for less frequently accessed workloads.
2. **EBS Features**
   * **Snapshots**: Incremental backups of EBS volumes stored in Amazon S3.
   * **Encryption**: Encrypt EBS volumes using AWS Key Management Service (KMS).
   * **Performance**: Provisioned IOPS for high performance, increased throughput for data-intensive applications.
3. **Managing EBS Volumes**
   * **Creation and Deletion**: Create volumes and attach them to EC2 instances, delete volumes when no longer needed.
   * **Resizing Volumes**: Increase the size, change the type, or modify IOPS of an existing volume.
   * **Attaching and Detaching**: Attach volumes to instances and detach when necessary.
4. **Best Practices**
   * **Snapshots for Backup**: Regular snapshots to ensure data durability.
   * **Encryption**: Use EBS encryption for sensitive data.
   * **Monitoring**: Use CloudWatch for monitoring EBS performance metrics.

***

**Security Groups**

1. **Functionality**
   * **Inbound and Outbound Rules**: Control inbound and outbound traffic to instances.
   * **Stateful Nature**: Return traffic is automatically allowed, regardless of inbound rules.
2. **Configuration**
   * **Creating Security Groups**: Define rules for different types of traffic.
   * **Associating with Instances**: Apply security groups to instances during launch or later.
3. **Best Practices**
   * **Least Privilege Principle**: Apply the principle of least privilege when defining rules.
   * **Regular Audits**: Regularly audit security group rules for compliance and security.
4. **Integration with Other Services**
   * **VPC Integration**: Security groups are used within VPCs to provide instance-level security.
   * **IAM Roles**: Combine with IAM roles for granular security.

***

**Auto Scaling**

1. **Components**
   * **Auto Scaling Groups (ASG)**: Define the minimum, maximum, and desired number of instances.
   * **Launch Configurations/Launch Templates**: Templates for launching new instances.
   * **Scaling Policies**: Define when and how to scale in or out.
2. **Types of Scaling**
   * **Dynamic Scaling**: Scale based on real-time demand.
   * **Scheduled Scaling**: Scale based on a schedule.
   * **Predictive Scaling**: Uses machine learning to predict future traffic and scale accordingly.
3. **Health Checks**
   * **EC2 Health Checks**: Ensure that instances are healthy and replace unhealthy instances.
   * **ELB Health Checks**: Use Elastic Load Balancer health checks to determine instance health.
4. **Best Practices**
   * **Capacity Planning**: Plan capacity for handling peak loads.
   * **Scaling Policies**: Use a combination of scaling policies for efficient scaling.
   * **Monitoring and Alerts**: Use CloudWatch for monitoring and setting up alerts.
5. **Integration with Other Services**
   * **Elastic Load Balancing (ELB)**: Distribute traffic across multiple instances.
   * **CloudWatch**: Monitor metrics and trigger scaling actions.

***

#### Summary

Amazon EC2 is a versatile and powerful compute service in AWS that offers a wide array of instance types to fit different use cases. Mastery of EC2 includes understanding instances, AMIs, EBS, security groups, and auto scaling, as well as integrating these components with other AWS services. By comprehensively understanding these elements, one can architect robust, scalable, and secure solutions on AWS, essential for success in the AWS Certified Solutions Architect - Professional exam.
