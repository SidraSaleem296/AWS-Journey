# AWS EBS

#### Detailed Notes on Amazon EBS for AWS Solution Architect Professional Exam

#### Introduction to Amazon EBS

Amazon Elastic Block Store (EBS) provides persistent block storage volumes for use with Amazon EC2 instances. EBS volumes are highly available and reliable storage volumes that can be attached to any running instance in the same Availability Zone.

#### Key Concepts

**1. EBS Volumes**

* **Definition**: EBS volumes are block-level storage devices that you can attach to your instances. They persist independently from the life of the instance.
* **Types of EBS Volumes**:
  * **General Purpose SSD (gp3/gp2)**: Cost-effective storage for a broad range of workloads.
  * **Provisioned IOPS SSD (io2/io1)**: High-performance SSD storage for mission-critical low-latency or high-throughput workloads.
  * **Throughput Optimized HDD (st1)**: Low-cost HDD designed for frequently accessed, throughput-intensive workloads.
  * **Cold HDD (sc1)**: Lowest cost HDD designed for less frequently accessed workloads.
  * **Magnetic (standard)**: Previous generation HDD, suitable for infrequent access workloads (not recommended for new volumes).

**2. Snapshots**

* **Definition**: Snapshots are incremental backups of EBS volumes, stored in Amazon S3. They capture only the changes since the last snapshot.
* **Use Cases**: Backups, disaster recovery, volume cloning, and data migration.

**3. EBS Volume Types and Use Cases**

* **General Purpose SSD (gp3)**:
  * **Use Case**: Recommended for most workloads, including boot volumes, virtual desktops, low-latency interactive apps, development and test environments.
  * **Performance**: Baseline performance of 3,000 IOPS, burstable to 16,000 IOPS.
* **Provisioned IOPS SSD (io2)**:
  * **Use Case**: Mission-critical applications, large databases, latency-sensitive transactional workloads.
  * **Performance**: Up to 256,000 IOPS per volume.
* **Throughput Optimized HDD (st1)**:
  * **Use Case**: Big data, data warehouses, log processing.
  * **Performance**: Baseline throughput of 40 MB/s per TB, up to 500 MB/s per volume.
* **Cold HDD (sc1)**:
  * **Use Case**: File storage, infrequently accessed data.
  * **Performance**: Baseline throughput of 12 MB/s per TB, up to 250 MB/s per volume.

**4. EBS Encryption**

* **Server-Side Encryption (SSE)**: EBS volumes can be encrypted at rest using AWS Key Management Service (KMS) keys.
* **Benefits**: Data is encrypted at rest, in transit, and during snapshots. Managed keys ensure security and compliance.
* **Misconception**: EBS encryption can only be enabled at volume creation. (Correction: Existing unencrypted volumes can be encrypted by creating an encrypted snapshot and restoring it to a new volume.)

**5. EBS Performance Optimization**

* **I/O Credits and Bursting**: General Purpose SSD volumes can burst up to 16,000 IOPS. I/O credits accumulate when the volume's IOPS are below the baseline performance.
* **Provisioned IOPS (PIOPS)**: For consistent, high-performance I/O, use io2 volumes with provisioned IOPS.
* **Elastic Volumes**: Allows you to dynamically change volume size, performance, and type without detaching the volume.

**6. EBS Multi-Attach**

* **Definition**: Allows multiple EC2 instances to simultaneously access a single io2 volume.
* **Use Cases**: Highly available applications, clustered databases.
* **Misconception**: Multi-Attach is available for all volume types. (Correction: Multi-Attach is only available for io2 volumes.)

**7. EBS Lifecycle Management**

* **Automated Snapshots**: Use Amazon Data Lifecycle Manager (DLM) to automate snapshot management.
* **Lifecycle Policies**: Define policies to create, retain, and delete EBS snapshots, reducing manual management and ensuring compliance.

**8. EBS Backups and Disaster Recovery**

* **Snapshots**: Incremental backups of EBS volumes.
* **Cross-Region Copy**: Snapshots can be copied to other regions to support disaster recovery.
* **Use Cases**: Regular backups, disaster recovery, volume migration.

**9. EBS Pricing**

* **Factors**: EBS pricing is based on the volume type, size, IOPS provisioned, and snapshots.
* **Optimization**: Choose the appropriate volume type based on workload requirements to optimize costs.

#### Integration with Other AWS Services

**1. Amazon EC2**

* **Use**: EBS volumes provide persistent storage for EC2 instances. Root volumes are typically EBS volumes.
* **Feature**: Elastic Volumes allow resizing and changing the volume type without stopping the instance.

**2. AWS Backup**

* **Integration**: EBS integrates with AWS Backup to provide a centralized backup solution across AWS services.
* **Features**: Automated backup schedules, lifecycle policies, and cross-region backup.

**3. AWS Lambda**

* **Integration**: EBS snapshots can be managed using Lambda functions for custom automation and orchestration.

**4. AWS CloudFormation**

* **Integration**: EBS volumes and snapshots can be provisioned and managed through CloudFormation templates for infrastructure as code (IaC).

**5. AWS Auto Scaling**

* **Integration**: EBS volumes can be used with Auto Scaling groups to dynamically adjust capacity based on demand.

#### Common Scenarios and Problem Statements

**Scenario 1: High-Performance Database Storage**

* **Problem**: A database application requires high IOPS and low latency.
* **Solution**: Use Provisioned IOPS SSD (io2) volumes to meet the performance requirements.

**Scenario 2: Cost-Effective Backup Solution**

* **Problem**: Regular backups of application data are needed, but budget is limited.
* **Solution**: Use General Purpose SSD (gp3) or Throughput Optimized HDD (st1) volumes for storage and automate snapshots with Amazon DLM.

**Scenario 3: Disaster Recovery Across Regions**

* **Problem**: Ensure data availability in case of a regional outage.
* **Solution**: Regularly copy EBS snapshots to another AWS region using cross-region snapshot copy.

**Scenario 4: Dynamic Workload Requirements**

* **Problem**: Application workloads change, requiring different storage performance at different times.
* **Solution**: Use Elastic Volumes to adjust volume size, performance, and type as needed without downtime.

**Scenario 5: Shared Storage for Clustered Applications**

* **Problem**: Multiple instances need concurrent read/write access to the same storage.
* **Solution**: Use EBS Multi-Attach with io2 volumes to allow multiple EC2 instances to access the volume simultaneously.

#### Misconceptions and Clarifications

**Misconception 1: EBS volumes can only be attached to one instance at a time.**

* **Correction**: EBS Multi-Attach allows io2 volumes to be attached to multiple instances simultaneously.

**Misconception 2: EBS volumes cannot be resized.**

* **Correction**: Elastic Volumes allow you to dynamically change volume size, performance, and type without detaching the volume.

**Misconception 3: EBS volumes cannot be encrypted after creation.**

* **Correction**: You can create an encrypted snapshot of an unencrypted volume and then restore it to a new encrypted volume.

**Misconception 4: Snapshots are full backups and consume a lot of storage.**

* **Correction**: Snapshots are incremental backups, and they only store changes made since the last snapshot.

**Misconception 5: EBS volumes automatically replicate across AZs.**

* **Correction**: EBS volumes are AZ-specific. Use EBS Snapshots and cross-AZ restores for redundancy.

#### Best Practices for Using Amazon EBS

1. **Choose the Right Volume Type**: Select the appropriate volume type (gp3, io2, st1, sc1) based on your workload’s performance and cost requirements.
2. **Monitor Performance**: Use Amazon CloudWatch to monitor EBS volume performance metrics.
3. **Use Snapshots for Backups**: Regularly create snapshots of your EBS volumes to protect against data loss.
4. **Implement Encryption**: Use EBS encryption for data at rest and in transit to meet security and compliance requirements.
5. **Automate Management**: Use Amazon Data Lifecycle Manager to automate the creation, retention, and deletion of EBS snapshots.
6. **Leverage Elastic Volumes**: Adjust volume size and performance without downtime using Elastic Volumes.
7. **Optimize Costs**: Monitor and optimize your EBS usage to control costs, choosing the right volume type and using snapshots efficiently.

By understanding these key concepts, use cases, misconceptions, and best practices, you will be well-prepared to utilize Amazon EBS effectively in real-world scenarios and for the AWS Solution Architect Professional exam.
