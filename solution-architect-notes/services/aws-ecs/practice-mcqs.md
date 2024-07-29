# Practice MCQs

#### Question Set:

1.  **Which ECS component is responsible for ensuring that a specified number of tasks are running and replacing tasks if they fail?**

    A. Clusters\
    B. Task Definitions\
    C. Services\
    D. Tasks

    **Answer:** C. Services\
    **Explanation:**

    * **Correct:** Services manage the number of running instances of a task and replace failed tasks.
    * **Incorrect:**
      * Clusters (A) are logical groupings of tasks or services.
      * Task Definitions (B) are blueprints for the application.
      * Tasks (D) are the instantiation of task definitions.
2.  **Which networking mode in ECS provides each task with an elastic network interface (ENI) directly in a VPC?**

    A. Bridge\
    B. Host\
    C. None\
    D. awsvpc

    **Answer:** D. awsvpc\
    **Explanation:**

    * **Correct:** The awsvpc mode provides each task with an ENI in the VPC.
    * **Incorrect:**
      * Bridge (A) uses Docker’s default bridge network.
      * Host (B) uses the host network of the EC2 instance.
      * None (C) disables networking for the task.
3.  **Which ECS mode is most cost-effective for applications with unpredictable traffic?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate can be more cost-effective for workloads with unpredictable traffic because it automatically scales without the need to manage instances.
    * **Incorrect:**
      * EC2 (A) can be cost-effective for consistent, high-volume workloads but requires more management.
      * Lambda (C) is not relevant in this context.
      * Beanstalk (D) is a different service for managing applications.
4.  **What is the primary benefit of using Amazon ECS with Fargate compared to using ECS with EC2 instances?**

    A. Lower cost for all workloads\
    B. No need to manage the underlying infrastructure\
    C. Better performance for high-volume workloads\
    D. More control over instance configuration

    **Answer:** B. No need to manage the underlying infrastructure\
    **Explanation:**

    * **Correct:** Fargate is a serverless compute engine, removing the need to manage infrastructure.
    * **Incorrect:**
      * Lower cost for all workloads (A) is not always true.
      * Better performance for high-volume workloads (C) is typically achieved with EC2.
      * More control over instance configuration (D) is a benefit of EC2 mode.
5.  **Which AWS service can be used with ECS to simplify discovering and connecting to microservices?**

    A. Amazon RDS\
    B. AWS X-Ray\
    C. Amazon S3\
    D. AWS Cloud Map

    **Answer:** D. AWS Cloud Map\
    **Explanation:**

    * **Correct:** AWS Cloud Map provides service discovery for ECS tasks.
    * **Incorrect:**
      * Amazon RDS (A) is for relational databases.
      * AWS X-Ray (B) is for tracing and analyzing request paths.
      * Amazon S3 (C) is for storage.
6.  **Which ECS component is described as a "blueprint" for your application, detailing the containers to run?**

    A. Tasks\
    B. Clusters\
    C. Task Definitions\
    D. Services

    **Answer:** C. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions describe the containers to run, including their configurations.
    * **Incorrect:**
      * Tasks (A) are the running instances of Task Definitions.
      * Clusters (B) are groupings of tasks or services.
      * Services (D) manage task instances.
7.  **How does ECS ensure high availability for services?**

    A. By using multiple clusters\
    B. By deploying tasks in different Availability Zones\
    C. By using multiple task definitions\
    D. By using multiple AWS regions

    **Answer:** B. By deploying tasks in different Availability Zones\
    **Explanation:**

    * **Correct:** Deploying tasks across multiple Availability Zones ensures high availability.
    * **Incorrect:**
      * Multiple clusters (A) manage tasks but do not inherently ensure high availability.
      * Multiple task definitions (C) are for different versions/configurations.
      * Multiple AWS regions (D) provide broader geographic distribution but are more complex to manage.
8.  **Which service is used to automatically scale the number of running ECS tasks based on load?**

    A. CloudWatch\
    B. Auto Scaling\
    C. Lambda\
    D. CloudFormation

    **Answer:** B. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling adjusts the number of running tasks based on specified metrics.
    * **Incorrect:**
      * CloudWatch (A) is for monitoring and logging.
      * Lambda (C) is for serverless compute.
      * CloudFormation (D) is for infrastructure as code.
9.  **What AWS service can be used to store and share files across multiple ECS tasks?**

    A. Amazon EBS\
    B. Amazon S3\
    C. Amazon EFS\
    D. AWS Backup

    **Answer:** C. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared file storage for ECS tasks.
    * **Incorrect:**
      * Amazon EBS (A) is block storage for individual instances.
      * Amazon S3 (B) is object storage.
      * AWS Backup (D) is for backup and restore services.
10. **Which component in ECS allows for running tasks without managing servers?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate is a serverless compute engine for containers, allowing tasks to run without managing servers.
    * **Incorrect:**
      * EC2 (A) requires managing servers.
      * Lambda (C) is for serverless functions, not containers.
      * Beanstalk (D) is a platform as a service.
11. **What is the primary benefit of using ECS with EC2 instances over Fargate?**

    A. Easier management\
    B. Lower cost for all workloads\
    C. More control over instance configuration\
    D. Serverless architecture

    **Answer:** C. More control over instance configuration\
    **Explanation:**

    * **Correct:** ECS with EC2 allows for detailed configuration of the instances.
    * **Incorrect:**
      * Easier management (A) is not accurate; Fargate offers easier management.
      * Lower cost for all workloads (B) depends on the specific use case.
      * Serverless architecture (D) describes Fargate, not EC2.
12. **Which networking mode in ECS uses the host network of the EC2 instance?**

    A. Bridge\
    B. Host\
    C. None\
    D. awsvpc

    **Answer:** B. Host\
    **Explanation:**

    * **Correct:** The host mode uses the network of the EC2 instance directly.
    * **Incorrect:**
      * Bridge (A) uses Docker’s default bridge network.
      * None (C) disables networking.
      * awsvpc (D) provides each task with an ENI.
13. **Which ECS feature allows you to securely store and manage sensitive information, such as database credentials?**

    A. IAM Roles\
    B. Secrets Manager\
    C. Security Groups\
    D. CloudWatch Logs

    **Answer:** B. Secrets Manager\
    **Explanation:**

    * **Correct:** Secrets Manager securely stores and manages sensitive information.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (C) control network access.
      * CloudWatch Logs (D) collect log data.
14. **How can you ensure that ECS tasks have the necessary permissions to access other AWS services?**

    A. Use IAM Roles for Tasks\
    B. Use Security Groups\
    C. Use CloudWatch Alarms\
    D. Use EC2 Key Pairs

    **Answer:** A. Use IAM Roles for Tasks\
    **Explanation:**

    * **Correct:** IAM Roles for Tasks provide the necessary permissions for ECS tasks.
    * **Incorrect:**
      * Security Groups (B) control network traffic, not permissions.
      * CloudWatch Alarms (C) monitor metrics and events.
      * EC2 Key Pairs (D) are for SSH access to instances.
15. **Which AWS service can be used to trace and analyze request paths across distributed applications, including those using ECS?**

    A. AWS X-Ray\
    B. AWS CloudTrail\
    C. AWS Config\
    D. Amazon Inspector

    **Answer:** A. AWS X-Ray\
    **Explanation:**

    * **Correct:** AWS X-Ray traces and analyzes request paths across distributed applications.
    * **Incorrect:**
      * AWS CloudTrail (B) records API calls.
      * AWS Config (C) monitors resource configurations.
      * Amazon Inspector (D) is for security assessments.
16. **Which ECS feature ensures that tasks only have the permissions necessary to perform their intended function?**

    A. Security Groups\
    B. IAM Roles for Tasks\
    C. Network ACLs\
    D. CloudWatch Logs

    **Answer:** B. IAM Roles for Tasks\
    **Explanation:**

    * **Correct:** IAM Roles for Tasks enforce the principle of least privilege.
    * **Incorrect:**
      * Security Groups (A) control network access.
      * Network ACLs (C) control network traffic at the subnet level.
      * CloudWatch Logs (D) collect log data.
17. **Which ECS feature allows you to define CPU and memory requirements for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions specify the CPU and memory requirements for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
18. **Which AWS service integrates with ECS to provide a centralized logging solution?**

    A. AWS CloudTrail\
    B. AWS Config\
    C. CloudWatch Logs\
    D. Amazon S3

    **Answer:** C. CloudWatch Logs\
    **Explanation:**

    * **Correct:** CloudWatch Logs collects and stores log data from ECS tasks.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (B) monitors resource configurations.
      * Amazon S3 (D) is object storage.
19. **Which ECS mode allows you to deploy containers on a cluster of Amazon EC2 instances?**

    A. Fargate\
    B. EC2\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. EC2\
    **Explanation:**

    * **Correct:** EC2 mode allows deploying containers on a cluster of EC2 instances.
    * **Incorrect:**
      * Fargate (A) is serverless for containers.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
20. **What is the primary benefit of using AWS Cloud Map with ECS?**

    A. Monitoring resource usage\
    B. Managing container logs\
    C. Simplifying service discovery\
    D. Automating task scaling

    **Answer:** C. Simplifying service discovery\
    **Explanation:**

    * **Correct:** AWS Cloud Map simplifies service discovery for ECS tasks.
    * **Incorrect:**
      * Monitoring resource usage (A) is done with CloudWatch.
      * Managing container logs (B) is done with CloudWatch Logs.
      * Automating task scaling (D) is done with Auto Scaling.
21. **Which ECS feature allows you to run containers without needing to provision and manage EC2 instances?**

    A. Elastic Load Balancing\
    B. Amazon RDS\
    C. Fargate\
    D. EC2

    **Answer:** C. Fargate\
    **Explanation:**

    * **Correct:** Fargate allows you to run containers without managing EC2 instances.
    * **Incorrect:**
      * Elastic Load Balancing (A) distributes traffic.
      * Amazon RDS (B) is for relational databases.
      * EC2 (D) requires managing instances.
22. **Which service allows ECS tasks to securely store and retrieve secrets?**

    A. IAM Roles\
    B. Security Groups\
    C. AWS Secrets Manager\
    D. CloudWatch Logs

    **Answer:** C. AWS Secrets Manager\
    **Explanation:**

    * **Correct:** AWS Secrets Manager securely stores and retrieves secrets.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (B) control network access.
      * CloudWatch Logs (D) collect log data.
23. **What is the main purpose of using ECS task definitions?**

    A. To define networking rules\
    B. To manage scaling of tasks\
    C. To describe container configurations\
    D. To store log data

    **Answer:** C. To describe container configurations\
    **Explanation:**

    * **Correct:** Task definitions describe container configurations, including CPU, memory, and Docker images.
    * **Incorrect:**
      * Networking rules (A) are managed with security groups and network modes.
      * Scaling of tasks (B) is managed with services and auto-scaling.
      * Storing log data (D) is done with CloudWatch Logs.
24. **Which AWS service can distribute traffic across multiple ECS tasks?**

    A. Amazon RDS\
    B. AWS CloudTrail\
    C. Elastic Load Balancing\
    D. AWS Config

    **Answer:** C. Elastic Load Balancing\
    **Explanation:**

    * **Correct:** Elastic Load Balancing distributes traffic across multiple ECS tasks.
    * **Incorrect:**
      * Amazon RDS (A) is for relational databases.
      * AWS CloudTrail (B) records API calls.
      * AWS Config (D) monitors resource configurations.
25. **Which ECS mode provides more control over the underlying instances and their configuration?**

    A. Fargate\
    B. Lambda\
    C. Beanstalk\
    D. EC2

    **Answer:** D. EC2\
    **Explanation:**

    * **Correct:** EC2 mode provides more control over the underlying instances and their configuration.
    * **Incorrect:**
      * Fargate (A) is serverless and does not provide control over instances.
      * Lambda (B) is for serverless functions.
      * Beanstalk (C) is a platform as a service.
26. **Which feature of ECS allows for the automatic adjustment of the number of running tasks based on predefined metrics?**

    A. CloudWatch Logs\
    B. Auto Scaling\
    C. IAM Roles\
    D. Security Groups

    **Answer:** B. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling automatically adjusts the number of running tasks based on predefined metrics.
    * **Incorrect:**
      * CloudWatch Logs (A) collect log data.
      * IAM Roles (C) manage permissions.
      * Security Groups (D) control network access.
27. **Which AWS service can be used to monitor the CPU and memory usage of ECS tasks?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch monitors CPU and memory usage of ECS tasks.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
28. **Which ECS component is responsible for grouping multiple services or tasks for management and monitoring?**

    A. Tasks\
    B. Task Definitions\
    C. Services\
    D. Clusters

    **Answer:** D. Clusters\
    **Explanation:**

    * **Correct:** Clusters group multiple services or tasks for management and monitoring.
    * **Incorrect:**
      * Tasks (A) are running instances of Task Definitions.
      * Task Definitions (B) describe container configurations.
      * Services (C) manage task instances.
29. **What is the primary purpose of using IAM roles with ECS tasks?**

    A. To control network access\
    B. To manage scaling of tasks\
    C. To assign permissions to tasks\
    D. To store log data

    **Answer:** C. To assign permissions to tasks\
    **Explanation:**

    * **Correct:** IAM roles assign permissions to ECS tasks, allowing them to access AWS resources securely.
    * **Incorrect:**
      * Network access (A) is controlled by security groups.
      * Scaling of tasks (B) is managed by services and auto-scaling.
      * Storing log data (D) is done with CloudWatch Logs.
30. **Which ECS feature allows you to define the Docker images, CPU, memory, and environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define the Docker images, CPU, memory, and environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
31. **Which ECS feature is used to distribute incoming traffic to ECS tasks, ensuring high availability and fault tolerance?**

    A. AWS CloudTrail\
    B. Elastic Load Balancing\
    C. AWS Config\
    D. CloudWatch Logs

    **Answer:** B. Elastic Load Balancing\
    **Explanation:**

    * **Correct:** Elastic Load Balancing distributes incoming traffic to ECS tasks, ensuring high availability and fault tolerance.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (C) monitors resource configurations.
      * CloudWatch Logs (D) collect log data.
32. **Which networking mode should you use if you want each ECS task to have its own elastic network interface (ENI) directly in a VPC?**

    A. Bridge\
    B. Host\
    C. None\
    D. awsvpc

    **Answer:** D. awsvpc\
    **Explanation:**

    * **Correct:** The awsvpc mode provides each task with an ENI directly in the VPC.
    * **Incorrect:**
      * Bridge (A) uses Docker’s default bridge network.
      * Host (B) uses the host network of the EC2 instance.
      * None (C) disables networking.
33. **What is the benefit of using AWS Secrets Manager with ECS?**

    A. Enhanced network performance\
    B. Easier log management\
    C. Secure storage of sensitive information\
    D. Simplified service discovery

    **Answer:** C. Secure storage of sensitive information\
    **Explanation:**

    * **Correct:** AWS Secrets Manager securely stores sensitive information, such as database credentials.
    * **Incorrect:**
      * Enhanced network performance (A) is not related.
      * Easier log management (B) is done with CloudWatch Logs.
      * Simplified service discovery (D) is achieved with AWS Cloud Map.
34. **Which feature allows ECS to automatically replace tasks if they fail?**

    A. IAM Roles\
    B. Auto Scaling\
    C. Services\
    D. CloudWatch Alarms

    **Answer:** C. Services\
    **Explanation:**

    * **Correct:** Services ensure the specified number of tasks are running and replace tasks if they fail.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Auto Scaling (B) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
35. **Which ECS feature helps to distribute incoming traffic evenly across multiple tasks to ensure high availability?**

    A. Task Definitions\
    B. Elastic Load Balancing\
    C. AWS Config\
    D. AWS X-Ray

    **Answer:** B. Elastic Load Balancing\
    **Explanation:**

    * **Correct:** Elastic Load Balancing distributes incoming traffic evenly across multiple tasks.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * AWS Config (C) monitors resource configurations.
      * AWS X-Ray (D) traces request paths.
36. **Which ECS feature allows you to define the number of desired tasks and ensure they are always running?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** B. Services\
    **Explanation:**

    * **Correct:** Services define the number of desired tasks and ensure they are always running.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
37. **What is the primary use of AWS X-Ray with ECS?**

    A. Monitor resource usage\
    B. Trace and analyze request paths\
    C. Store and manage secrets\
    D. Control network access

    **Answer:** B. Trace and analyze request paths\
    **Explanation:**

    * **Correct:** AWS X-Ray traces and analyzes request paths across distributed applications.
    * **Incorrect:**
      * Monitor resource usage (A) is done with CloudWatch.
      * Store and manage secrets (C) is done with Secrets Manager.
      * Control network access (D) is done with Security Groups.
38. **Which AWS service can be used to trigger ECS tasks based on S3 events?**

    A. AWS Lambda\
    B. AWS CloudTrail\
    C. AWS Config\
    D. Amazon S3

    **Answer:** A. AWS Lambda\
    **Explanation:**

    * **Correct:** AWS Lambda can trigger ECS tasks based on events from S3.
    * **Incorrect:**
      * AWS CloudTrail (B) records API calls.
      * AWS Config (C) monitors resource configurations.
      * Amazon S3 (D) is the source of the events, not the trigger mechanism.
39. **Which feature allows you to control network traffic for ECS tasks?**

    A. IAM Roles\
    B. Security Groups\
    C. CloudWatch Logs\
    D. Task Definitions

    **Answer:** B. Security Groups\
    **Explanation:**

    * **Correct:** Security Groups control network traffic for ECS tasks.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * CloudWatch Logs (C) collect log data.
      * Task Definitions (D) describe container configurations.
40. **Which ECS mode should be used if you want a serverless solution for running containers?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate is the serverless mode for running containers in ECS.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
41. **Which ECS feature allows for the creation of containerized applications that can securely connect to Amazon RDS?**

    A. Security Groups\
    B. Task Definitions\
    C. IAM Roles\
    D. Clusters

    **Answer:** C. IAM Roles\
    **Explanation:**

    * **Correct:** IAM Roles provide secure access to Amazon RDS for ECS tasks.
    * **Incorrect:**
      * Security Groups (A) control network access.
      * Task Definitions (B) describe container configurations.
      * Clusters (D) group tasks and services.
42. **What is the purpose of using CloudWatch Alarms with ECS?**

    A. To trace request paths\
    B. To monitor and alert on metrics\
    C. To manage secrets\
    D. To control network access

    **Answer:** B. To monitor and alert on metrics\
    **Explanation:**

    * **Correct:** CloudWatch Alarms monitor metrics and alert based on thresholds.
    * **Incorrect:**
      * Trace request paths (A) is done with AWS X-Ray.
      * Manage secrets (C) is done with Secrets Manager.
      * Control network access (D) is done with Security Groups.
43. **Which ECS feature can be used to define environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
44. **Which AWS service can be used to collect and analyze logs from ECS tasks?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch Logs\
    D. AWS Lambda

    **Answer:** C. CloudWatch Logs\
    **Explanation:**

    * **Correct:** CloudWatch Logs collects and analyzes logs from ECS tasks.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
45. **Which feature in ECS allows you to update your services with minimal downtime?**

    A. Task Definitions\
    B. Rolling Updates\
    C. Clusters\
    D. Tasks

    **Answer:** B. Rolling Updates\
    **Explanation:**

    * **Correct:** Rolling Updates allow for updating services with minimal downtime.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
46. **Which ECS feature provides shared file storage that can be accessed by multiple tasks?**

    A. Amazon RDS\
    B. Amazon EBS\
    C. Amazon EFS\
    D. AWS Backup

    **Answer:** C. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared file storage accessible by multiple tasks.
    * **Incorrect:**
      * Amazon RDS (A) is for relational databases.
      * Amazon EBS (B) provides block storage for individual instances.
      * AWS Backup (D) is for backup and restore services.
47. **Which AWS service integrates with ECS to provide monitoring and alerting on resource usage?**

    A. AWS Config\
    B. AWS CloudTrail\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch provides monitoring and alerting on resource usage for ECS tasks.
    * **Incorrect:**
      * AWS Config (A) monitors resource configurations.
      * AWS CloudTrail (B) records API calls.
      * AWS Lambda (D) is for serverless functions.
48. **Which ECS component describes the containers to run, including their configurations?**

    A. Tasks\
    B. Clusters\
    C. Task Definitions\
    D. Services

    **Answer:** C. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions describe the containers to run, including their configurations.
    * **Incorrect:**
      * Tasks (A) are the running instances of Task Definitions.
      * Clusters (B) group tasks and services.
      * Services (D) manage task instances.
49. **Which AWS service can be used with ECS to automate the backup and restore of data?**

    A. Amazon RDS\
    B. AWS Backup\
    C. AWS Config\
    D. CloudWatch

    **Answer:** B. AWS Backup\
    **Explanation:**

    * **Correct:** AWS Backup automates the backup and restore of data.
    * **Incorrect:**
      * Amazon RDS (A) provides managed relational databases.
      * AWS Config (C) monitors resource configurations.
      * CloudWatch (D) provides monitoring and alerting.
50. **What is the primary benefit of using IAM Roles with ECS tasks?**

    A. To manage scaling of tasks\
    B. To assign granular permissions to tasks\
    C. To collect and analyze logs\
    D. To control network traffic

    **Answer:** B. To assign granular permissions to tasks\
    **Explanation:**

    * **Correct:** IAM Roles assign granular permissions to ECS tasks, allowing secure access to AWS resources.
    * **Incorrect:**
      * Scaling of tasks (A) is managed by services and auto-scaling.
      * Collecting and analyzing logs (C) is done with CloudWatch Logs.
      * Controlling network traffic (D) is done with Security Groups.
51. **Which feature in ECS ensures that a specified number of tasks are always running?**

    A. Task Definitions\
    B. Auto Scaling\
    C. Services\
    D. CloudWatch Alarms

    **Answer:** C. Services\
    **Explanation:**

    * **Correct:** Services ensure that a specified number of tasks are always running.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Auto Scaling (B) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
52. **Which ECS feature allows you to define resource limits for CPU and memory for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define resource limits for CPU and memory for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
53. **Which AWS service can be used to trace and analyze request paths in distributed applications, including ECS?**

    A. AWS X-Ray\
    B. AWS Config\
    C. AWS CloudTrail\
    D. AWS Lambda

    **Answer:** A. AWS X-Ray\
    **Explanation:**

    * **Correct:** AWS X-Ray traces and analyzes request paths in distributed applications, including ECS.
    * **Incorrect:**
      * AWS Config (B) monitors resource configurations.
      * AWS CloudTrail (C) records API calls.
      * AWS Lambda (D) is for serverless functions.
54. **Which ECS feature allows you to automatically scale the number of running tasks based on predefined metrics?**

    A. IAM Roles\
    B. Auto Scaling\
    C. Security Groups\
    D. Task Definitions

    **Answer:** B. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling automatically adjusts the number of running tasks based on predefined metrics.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (C) control network access.
      * Task Definitions (D) describe container configurations.
55. **Which ECS mode should you use if you need detailed control over the underlying infrastructure and instance configuration?**

    A. Fargate\
    B. EC2\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. EC2\
    **Explanation:**

    * **Correct:** EC2 mode provides detailed control over the underlying infrastructure and instance configuration.
    * **Incorrect:**
      * Fargate (A) is serverless and does not provide control over instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
56. **Which AWS service can distribute incoming traffic to ECS tasks to ensure high availability?**

    A. Amazon RDS\
    B. AWS CloudTrail\
    C. Elastic Load Balancing\
    D. AWS Config

    **Answer:** C. Elastic Load Balancing\
    **Explanation:**

    * **Correct:** Elastic Load Balancing distributes incoming traffic to ECS tasks, ensuring high availability.
    * **Incorrect:**
      * Amazon RDS (A) is for relational databases.
      * AWS CloudTrail (B) records API calls.
      * AWS Config (D) monitors resource configurations.
57. **Which feature in ECS provides shared storage that can be accessed by multiple tasks across different instances?**

    A. Amazon EFS\
    B. Amazon RDS\
    C. Amazon S3\
    D. AWS Backup

    **Answer:** A. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared storage that can be accessed by multiple tasks across different instances.
    * **Incorrect:**
      * Amazon RDS (B) is for relational databases.
      * Amazon S3 (C) is object storage.
      * AWS Backup (D) is for backup and restore services.
58. **What is the primary use of AWS Secrets Manager with ECS?**

    A. To manage scaling of tasks\
    B. To store and manage sensitive information securely\
    C. To control network access\
    D. To collect and analyze logs

    **Answer:** B. To store and manage sensitive information securely\
    **Explanation:**

    * **Correct:** AWS Secrets Manager stores and manages sensitive information securely.
    * **Incorrect:**
      * Scaling of tasks (A) is managed by services and auto-scaling.
      * Controlling network access (C) is done with Security Groups.
      * Collecting and analyzing logs (D) is done with CloudWatch Logs.
59. **Which ECS feature allows you to define the Docker images and environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define the Docker images and environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
60. **Which AWS service integrates with ECS to provide monitoring and alerting on task resource usage?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch provides monitoring and alerting on task resource usage.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
61. **Which feature of ECS allows you to automatically replace failed tasks to maintain desired service levels?**

    A. Task Definitions\
    B. Services\
    C. Auto Scaling\
    D. CloudWatch Alarms

    **Answer:** B. Services\
    **Explanation:**

    * **Correct:** Services automatically replace failed tasks to maintain desired service levels.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Auto Scaling (C) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
62. **Which ECS mode should be used if you want to run containers without managing the underlying infrastructure?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate allows running containers without managing the underlying infrastructure.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
63. **Which AWS service can be used to securely store and manage database credentials for ECS tasks?**

    A. Amazon RDS\
    B. AWS Secrets Manager\
    C. AWS Config\
    D. AWS CloudTrail

    **Answer:** B. AWS Secrets Manager\
    **Explanation:**

    * **Correct:** AWS Secrets Manager securely stores and manages database credentials.
    * **Incorrect:**
      * Amazon RDS (A) provides managed relational databases.
      * AWS Config (C) monitors resource configurations.
      * AWS CloudTrail (D) records API calls.
64. **Which feature in ECS ensures that tasks have the necessary permissions to access other AWS services?**

    A. Security Groups\
    B. IAM Roles for Tasks\
    C. CloudWatch Logs\
    D. Task Definitions

    **Answer:** B. IAM Roles for Tasks\
    **Explanation:**

    * **Correct:** IAM Roles for Tasks ensure that tasks have the necessary permissions to access other AWS services.
    * **Incorrect:**
      * Security Groups (A) control network access.
      * CloudWatch Logs (C) collect log data.
      * Task Definitions (D) describe container configurations.
65. **Which ECS component groups multiple services or tasks for easier management and monitoring?**

    A. Tasks\
    B. Task Definitions\
    C. Services\
    D. Clusters

    **Answer:** D. Clusters\
    **Explanation:**

    * **Correct:** Clusters group multiple services or tasks for easier management and monitoring.
    * **Incorrect:**
      * Tasks (A) are running instances of Task Definitions.
      * Task Definitions (B) describe container configurations.
      * Services (C) manage task instances.
66. **Which ECS feature allows you to define CPU and memory requirements for containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define CPU and memory requirements for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are the running instances of Task Definitions.
67. **Which AWS service integrates with ECS to provide centralized logging for tasks?**

    A. AWS CloudTrail\
    B. AWS Config\
    C. CloudWatch Logs\
    D. AWS Lambda

    **Answer:** C. CloudWatch Logs\
    **Explanation:**

    * **Correct:** CloudWatch Logs provides centralized logging for ECS tasks.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
68. **Which ECS feature allows you to securely store and manage secrets such as API keys and database credentials?**

    A. IAM Roles\
    B. AWS Secrets Manager\
    C. Security Groups\
    D. CloudWatch Logs

    **Answer:** B. AWS Secrets Manager\
    **Explanation:**

    * **Correct:** AWS Secrets Manager securely stores and manages secrets such as API keys and database credentials.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (C) control network access.
      * CloudWatch Logs (D) collect log data.
69. **Which ECS mode provides a serverless compute engine for running containers?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate provides a serverless compute engine for running containers.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
70. **Which ECS component describes the Docker images, CPU, memory, and environment variables for your containers?**

    A. Tasks\
    B. Clusters\
    C. Task Definitions\
    D. Services

    **Answer:** C. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions describe the Docker images, CPU, memory, and environment variables for containers.
    * **Incorrect:**
      * Tasks (A) are running instances of Task Definitions.
      * Clusters (B) group tasks and services.
      * Services (D) manage task instances.
71. **Which AWS service can be used to distribute incoming traffic across multiple ECS tasks?**

    A. AWS CloudTrail\
    B. Amazon RDS\
    C. Elastic Load Balancing\
    D. AWS Config

    **Answer:** C. Elastic Load Balancing\
    **Explanation:**

    * **Correct:** Elastic Load Balancing distributes incoming traffic across multiple ECS tasks.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * Amazon RDS (B) is for relational databases.
      * AWS Config (D) monitors resource configurations.
72. **Which feature in ECS allows you to automatically adjust the number of running tasks based on load?**

    A. Task Definitions\
    B. Services\
    C. Auto Scaling\
    D. CloudWatch Alarms

    **Answer:** C. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling automatically adjusts the number of running tasks based on load.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Services (B) manage task instances.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
73. **Which ECS mode should be used if you need more control over the instance configuration and underlying infrastructure?**

    A. Fargate\
    B. EC2\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. EC2\
    **Explanation:**

    * **Correct:** EC2 mode provides more control over the instance configuration and underlying infrastructure.
    * **Incorrect:**
      * Fargate (A) is serverless and does not provide control over instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
74. **Which AWS service can be used to monitor CPU and memory usage of ECS tasks?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch monitors CPU and memory usage of ECS tasks.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
75. **Which ECS feature allows you to define environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are running instances of Task Definitions.
76. **Which feature in ECS ensures that a specified number of tasks are always running and replaces failed tasks?**

    A. Task Definitions\
    B. Services\
    C. Auto Scaling\
    D. CloudWatch Alarms

    **Answer:** B. Services\
    **Explanation:**

    * **Correct:** Services ensure that a specified number of tasks are always running and replace failed tasks.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Auto Scaling (C) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
77. **Which AWS service integrates with ECS to provide tracing and analysis of request paths in distributed applications?**

    A. AWS CloudTrail\
    B. AWS Config\
    C. AWS X-Ray\
    D. AWS Lambda

    **Answer:** C. AWS X-Ray\
    **Explanation:**

    * **Correct:** AWS X-Ray provides tracing and analysis of request paths in distributed applications.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
78. **Which ECS feature provides shared storage that can be accessed by multiple tasks across different instances?**

    A. Amazon EFS\
    B. Amazon RDS\
    C. Amazon S3\
    D. AWS Backup

    **Answer:** A. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared storage that can be accessed by multiple tasks across different instances.
    * **Incorrect:**
      * Amazon RDS (B) is for relational databases.
      * Amazon S3 (C) is object storage.
      * AWS Backup (D) is for backup and restore services.
79. **Which ECS mode should be used if you want to run containers without managing the underlying instances?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate allows running containers without managing the underlying instances.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
80. **Which AWS service integrates with ECS to automate the backup and restore of data?**

    A. Amazon RDS\
    B. AWS Backup\
    C. AWS Config\
    D. CloudWatch

    **Answer:** B. AWS Backup\
    **Explanation:**

    * **Correct:** AWS Backup automates the backup and restore of data.
    * **Incorrect:**
      * Amazon RDS (A) provides managed relational databases.
      * AWS Config (C) monitors resource configurations.
      * CloudWatch (D) provides monitoring and alerting.
81. **Which ECS feature allows you to automatically scale the number of running tasks based on predefined metrics?**

    A. IAM Roles\
    B. Auto Scaling\
    C. Security Groups\
    D. Task Definitions

    **Answer:** B. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling automatically adjusts the number of running tasks based on predefined metrics.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (C) control network access.
      * Task Definitions (D) describe container configurations.
82. **Which ECS component is responsible for grouping multiple services or tasks for management and monitoring?**

    A. Tasks\
    B. Task Definitions\
    C. Services\
    D. Clusters

    **Answer:** D. Clusters\
    **Explanation:**

    * **Correct:** Clusters group multiple services or tasks for management and monitoring.
    * **Incorrect:**
      * Tasks (A) are running instances of Task Definitions.
      * Task Definitions (B) describe container configurations.
      * Services (C) manage task instances.
83. **Which ECS mode provides a serverless compute engine for running containers?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate provides a serverless compute engine for running containers.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
84. **Which AWS service can be used to monitor CPU and memory usage of ECS tasks?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch monitors CPU and memory usage of ECS tasks.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
85. **Which ECS feature allows you to define environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are running instances of Task Definitions.
86. **Which feature in ECS ensures that a specified number of tasks are always running and replaces failed tasks?**

    A. Task Definitions\
    B. Services\
    C. Auto Scaling\
    D. CloudWatch Alarms

    **Answer:** B. Services\
    **Explanation:**

    * **Correct:** Services ensure that a specified number of tasks are always running and replace failed tasks.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Auto Scaling (C) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
87. **Which AWS service integrates with ECS to provide tracing and analysis of request paths in distributed applications?**

    A. AWS CloudTrail\
    B. AWS Config\
    C. AWS X-Ray\
    D. AWS Lambda

    **Answer:** C. AWS X-Ray\
    **Explanation:**

    * **Correct:** AWS X-Ray provides tracing and analysis of request paths in distributed applications.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
88. **Which ECS feature provides shared storage that can be accessed by multiple tasks across different instances?**

    A. Amazon EFS\
    B. Amazon RDS\
    C. Amazon S3\
    D. AWS Backup

    **Answer:** A. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared storage that can be accessed by multiple tasks across different instances.
    * **Incorrect:**
      * Amazon RDS (B) is for relational databases.
      * Amazon S3 (C) is object storage.
      * AWS Backup (D) is for backup and restore services.
89. **Which ECS mode should be used if you want to run containers without managing the underlying instances?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate allows running containers without managing the underlying instances.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
90. **Which AWS service integrates with ECS to automate the backup and restore of data?**

    A. Amazon RDS\
    B. AWS Backup\
    C. AWS Config\
    D. CloudWatch

    **Answer:** B. AWS Backup\
    **Explanation:**

    * **Correct:** AWS Backup automates the backup and restore of data.
    * **Incorrect:**
      * Amazon RDS (A) provides managed relational databases.
      * AWS Config (C) monitors resource configurations.
      * CloudWatch (D) provides monitoring and alerting.
91. **Which ECS feature allows you to automatically scale the number of running tasks based on predefined metrics?**

    A. IAM Roles\
    B. Auto Scaling\
    C. Security Groups\
    D. Task Definitions

    **Answer:** B. Auto Scaling\
    **Explanation:**

    * **Correct:** Auto Scaling automatically adjusts the number of running tasks based on predefined metrics.
    * **Incorrect:**
      * IAM Roles (A) manage permissions.
      * Security Groups (C) control network access.
      * Task Definitions (D) describe container configurations.
92. **Which ECS component is responsible for grouping multiple services or tasks for management and monitoring?**

    A. Tasks\
    B. Task Definitions\
    C. Services\
    D. Clusters

    **Answer:** D. Clusters\
    **Explanation:**

    * **Correct:** Clusters group multiple services or tasks for management and monitoring.
    * **Incorrect:**
      * Tasks (A) are running instances of Task Definitions.
      * Task Definitions (B) describe container configurations.
      * Services (C) manage task instances.
93. **Which ECS mode provides a serverless compute engine for running containers?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate provides a serverless compute engine for running containers.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
94. **Which AWS service can be used to monitor CPU and memory usage of ECS tasks?**

    A. AWS X-Ray\
    B. AWS Config\
    C. CloudWatch\
    D. AWS Lambda

    **Answer:** C. CloudWatch\
    **Explanation:**

    * **Correct:** CloudWatch monitors CPU and memory usage of ECS tasks.
    * **Incorrect:**
      * AWS X-Ray (A) traces request paths.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
95. **Which ECS feature allows you to define environment variables for your containers?**

    A. Task Definitions\
    B. Services\
    C. Clusters\
    D. Tasks

    **Answer:** A. Task Definitions\
    **Explanation:**

    * **Correct:** Task Definitions define environment variables for containers.
    * **Incorrect:**
      * Services (B) manage task instances.
      * Clusters (C) group tasks and services.
      * Tasks (D) are running instances of Task Definitions.
96. **Which feature in ECS ensures that a specified number of tasks are always running and replaces failed tasks?**

    A. Task Definitions\
    B. Services\
    C. Auto Scaling\
    D. CloudWatch Alarms

    **Answer:** B. Services\
    **Explanation:**

    * **Correct:** Services ensure that a specified number of tasks are always running and replace failed tasks.
    * **Incorrect:**
      * Task Definitions (A) describe container configurations.
      * Auto Scaling (C) adjusts the number of running tasks based on load.
      * CloudWatch Alarms (D) monitor metrics and trigger actions.
97. **Which AWS service integrates with ECS to provide tracing and analysis of request paths in distributed applications?**

    A. AWS CloudTrail\
    B. AWS Config\
    C. AWS X-Ray\
    D. AWS Lambda

    **Answer:** C. AWS X-Ray\
    **Explanation:**

    * **Correct:** AWS X-Ray provides tracing and analysis of request paths in distributed applications.
    * **Incorrect:**
      * AWS CloudTrail (A) records API calls.
      * AWS Config (B) monitors resource configurations.
      * AWS Lambda (D) is for serverless functions.
98. **Which ECS feature provides shared storage that can be accessed by multiple tasks across different instances?**

    A. Amazon EFS\
    B. Amazon RDS\
    C. Amazon S3\
    D. AWS Backup

    **Answer:** A. Amazon EFS\
    **Explanation:**

    * **Correct:** Amazon EFS provides shared storage that can be accessed by multiple tasks across different instances.
    * **Incorrect:**
      * Amazon RDS (B) is for relational databases.
      * Amazon S3 (C) is object storage.
      * AWS Backup (D) is for backup and restore services.
99. **Which ECS mode should be used if you want to run containers without managing the underlying instances?**

    A. EC2\
    B. Fargate\
    C. Lambda\
    D. Beanstalk

    **Answer:** B. Fargate\
    **Explanation:**

    * **Correct:** Fargate allows running containers without managing the underlying instances.
    * **Incorrect:**
      * EC2 (A) requires managing instances.
      * Lambda (C) is for serverless functions.
      * Beanstalk (D) is a platform as a service.
