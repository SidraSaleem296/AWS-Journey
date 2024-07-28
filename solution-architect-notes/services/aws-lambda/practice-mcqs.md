# Practice MCQs

#### AWS Lambda: Key Concepts and Example Scenarios

1.  **Which AWS service can be used to trigger a Lambda function upon the creation of a new object in an S3 bucket?**

    * A) Amazon RDS
    * B) Amazon SNS
    * C) Amazon S3
    * D) Amazon EC2

    **Answer: C) Amazon S3**

    * **Explanation**: Amazon S3 can trigger Lambda functions upon events such as object creation.
    * **Incorrect Options**:
      * **A) Amazon RDS**: This service is for relational database management, not event triggering.
      * **B) Amazon SNS**: SNS can trigger Lambda functions, but the scenario specifies S3 events.
      * **D) Amazon EC2**: EC2 is for virtual servers, not for event triggering.
2.  **What is the role of the handler in a Lambda function?**

    * A) To define the runtime environment
    * B) To specify the memory allocation
    * C) To process input and produce output
    * D) To manage environment variables

    **Answer: C) To process input and produce output**

    * **Explanation**: The handler is the entry point for Lambda function execution.
    * **Incorrect Options**:
      * **A) To define the runtime environment**: The runtime environment is defined separately.
      * **B) To specify the memory allocation**: Memory allocation is set in the function configuration.
      * **D) To manage environment variables**: Environment variables are managed separately from the handler.
3.  **Which of the following runtimes is not natively supported by AWS Lambda?**

    * A) Node.js
    * B) Python
    * C) Ruby
    * D) PHP

    **Answer: D) PHP**

    * **Explanation**: PHP is not natively supported as a runtime in AWS Lambda.
    * **Incorrect Options**:
      * **A) Node.js**: Supported runtime.
      * **B) Python**: Supported runtime.
      * **C) Ruby**: Supported runtime.
4.  **How can custom applications trigger AWS Lambda functions?**

    * A) By direct invocation via AWS SDKs
    * B) By sending email notifications
    * C) By creating an S3 bucket
    * D) By starting an EC2 instance

    **Answer: A) By direct invocation via AWS SDKs**

    * **Explanation**: Custom applications can trigger Lambda functions via SDKs.
    * **Incorrect Options**:
      * **B) By sending email notifications**: Emails do not directly trigger Lambda functions.
      * **C) By creating an S3 bucket**: This action does not trigger Lambda functions.
      * **D) By starting an EC2 instance**: This action does not directly trigger Lambda functions.
5.  **What is the maximum execution timeout for a Lambda function?**

    * A) 1 minute
    * B) 5 minutes
    * C) 15 minutes
    * D) 30 minutes

    **Answer: C) 15 minutes**

    * **Explanation**: The maximum execution time for a Lambda function is 15 minutes.
    * **Incorrect Options**:
      * **A) 1 minute**: Incorrect timeout limit.
      * **B) 5 minutes**: Incorrect timeout limit.
      * **D) 30 minutes**: Exceeds the allowed timeout limit.
6.  **What does setting the reserved concurrency for a Lambda function do?**

    * A) Ensures the function runs faster
    * B) Limits the maximum number of concurrent executions
    * C) Allocates more memory to the function
    * D) Triggers the function more frequently

    **Answer: B) Limits the maximum number of concurrent executions**

    * **Explanation**: Reserved concurrency limits the number of concurrent executions to ensure other functions have resources.
    * **Incorrect Options**:
      * **A) Ensures the function runs faster**: Concurrency does not affect execution speed.
      * **C) Allocates more memory to the function**: Memory allocation is separate from concurrency settings.
      * **D) Triggers the function more frequently**: Concurrency settings do not affect trigger frequency.
7.  **How can you ensure that a Lambda function has the permissions needed to access AWS services and resources?**

    * A) By assigning an execution role with the necessary permissions
    * B) By adding permissions in the function code
    * C) By using environment variables
    * D) By configuring the Lambda function in a VPC

    **Answer: A) By assigning an execution role with the necessary permissions**

    * **Explanation**: An execution role with the necessary permissions grants Lambda access to AWS services and resources.
    * **Incorrect Options**:
      * **B) By adding permissions in the function code**: Permissions cannot be added in the function code.
      * **C) By using environment variables**: Environment variables do not grant permissions.
      * **D) By configuring the Lambda function in a VPC**: VPC configuration does not grant permissions.
8.  **What is the purpose of Lambda Layers?**

    * A) To store environment variables
    * B) To manage VPC configurations
    * C) To package libraries and dependencies
    * D) To allocate memory dynamically

    **Answer: C) To package libraries and dependencies**

    * **Explanation**: Lambda Layers are used to package libraries, custom runtimes, or other dependencies.
    * **Incorrect Options**:
      * **A) To store environment variables**: Environment variables are not stored in layers.
      * **B) To manage VPC configurations**: VPC configurations are managed separately.
      * **D) To allocate memory dynamically**: Memory allocation is managed in the function configuration.
9.  **Which option allows you to process and analyze real-time data streams in AWS Lambda?**

    * A) AWS Glue
    * B) Amazon Kinesis
    * C) AWS DMS
    * D) Amazon S3

    **Answer: B) Amazon Kinesis**

    * **Explanation**: Amazon Kinesis can be used to process and analyze real-time data streams with Lambda.
    * **Incorrect Options**:
      * **A) AWS Glue**: Primarily used for ETL processes.
      * **C) AWS DMS**: Used for database migration.
      * **D) Amazon S3**: Not primarily used for real-time data processing.
10. **What happens to the data on an instance store volume when a Lambda function is stopped?**

    * A) The data is preserved
    * B) The data is deleted
    * C) The data is backed up automatically
    * D) The data is migrated to an EBS volume

    **Answer: B) The data is deleted**

    * **Explanation**: Instance store volumes are ephemeral; data is lost when the instance is stopped.
    * **Incorrect Options**:
      * **A) The data is preserved**: Instance store data is not preserved.
      * **C) The data is backed up automatically**: No automatic backup for instance store data.
      * **D) The data is migrated to an EBS volume**: Data is not automatically migrated.

#### Configuration and Management

11. **How does memory allocation affect a Lambda function's performance?**

    * A) More memory only increases storage capacity
    * B) More memory increases CPU power, which can improve performance
    * C) More memory reduces the function's execution timeout
    * D) More memory decreases the function's concurrency limit

    **Answer: B) More memory increases CPU power, which can improve performance**

    * **Explanation**: Allocating more memory increases CPU power, potentially improving performance.
    * **Incorrect Options**:
      * **A) More memory only increases storage capacity**: Memory allocation affects CPU power as well.
      * **C) More memory reduces the function's execution timeout**: Timeout settings are independent of memory allocation.
      * **D) More memory decreases the function's concurrency limit**: Concurrency limit is set separately.
12. **What is the maximum memory allocation for a Lambda function?**

    * A) 512 MB
    * B) 2048 MB
    * C) 4096 MB
    * D) 10240 MB

    **Answer: D) 10240 MB**

    * **Explanation**: The maximum memory allocation for a Lambda function is 10,240 MB.
    * **Incorrect Options**:
      * **A) 512 MB**: Incorrect memory limit.
      * **B) 2048 MB**: Incorrect memory limit.
      * **C) 4096 MB**: Incorrect memory limit.
13. **What does setting the timeout for a Lambda function control?**

    * A) The maximum amount of memory the function can use
    * B) The duration the function can run before being forcibly terminated
    * C) The maximum number of concurrent executions allowed
    * D) The number of retries on failure

    **Answer: B) The duration the function can run before being forcibly terminated**

    * **Explanation**: Timeout setting controls how long a function can run before being forcibly terminated.
    * **Incorrect Options**:
      * **A) The maximum amount of memory the function can use**: Memory allocation is managed separately.
      * **C) The maximum number of concurrent executions allowed**: Concurrency is set separately.
      * **D) The number of retries on failure**: Retries are configured separately.
14. **What does provisioned concurrency ensure for a Lambda function?**

    * A) Limits the number of concurrent executions
    * B) Initializes a specific number of function instances to be ready to respond instantly
    * C) Automatically adjusts memory allocation based on workload
    * D) Sets a fixed execution timeout

    **Answer: B) Initializes a specific number of function instances to be ready to respond instantly**

    * **Explanation**: Provisioned concurrency ensures a specific number of function instances are ready to respond instantly.
    * **Incorrect Options**:
      * **A) Limits the number of concurrent executions**: Reserved concurrency limits concurrent executions.
      * **C) Automatically adjusts memory allocation based on workload**: Memory allocation is managed separately.
      * **D) Sets a fixed execution timeout**: Timeout is configured separately.
15. **What is the main purpose of using a Dead Letter Queue (DLQ) with Lambda functions?**

    * A) To increase function concurrency
    * B) To send failed execution records to SQS or SNS for analysis
    * C) To extend the function's execution timeout
    * D) To automatically retry failed executions

    **Answer: B) To send failed execution records to SQS or SNS for analysis**

    * **Explanation**: DLQ sends failed execution records to SQS or SNS for further analysis.
    * **Incorrect Options**:
      * **A) To increase function concurrency**: DLQ does not affect concurrency.
      * **C) To extend the function's execution timeout**: DLQ does not affect timeout.
      * **D) To automatically retry failed executions**: Retries are configured separately.
16. **How many times does Lambda retry failed executions by default for asynchronous invocations?**

    * A) Once
    * B) Twice
    * C) Three times
    * D) Four times

    **Answer: B) Twice**

    * **Explanation**: By default, Lambda retries failed executions twice for asynchronous invocations.
    * **Incorrect Options**:
      * **A) Once**: Incorrect number of retries.
      * **C) Three times**: Incorrect number of retries.
      * **D) Four times**: Incorrect number of retries.
17. **What information is provided by AWS X-Ray for Lambda functions?**

    * A) Execution time and memory usage
    * B) Trace and analyze request paths to troubleshoot performance issues
    * C) Function configuration details
    * D) Network traffic details

    **Answer: B) Trace and analyze request paths to troubleshoot performance issues**

    * **Explanation**: AWS X-Ray provides tracing and analysis of request paths to troubleshoot performance issues.
    * **Incorrect Options**:
      * **A) Execution time and memory usage**: Provided by CloudWatch Metrics.
      * **C) Function configuration details**: Managed in the Lambda console.
      * **D) Network traffic details**: X-Ray focuses on request tracing, not network traffic details.
18. **What is the main benefit of integrating Lambda with CloudWatch Logs?**

    * A) To automatically retry failed invocations
    * B) To log function invocations and errors
    * C) To increase function concurrency
    * D) To extend the execution timeout

    **Answer: B) To log function invocations and errors**

    * **Explanation**: CloudWatch Logs is used to log Lambda function invocations and errors for monitoring and troubleshooting.
    * **Incorrect Options**:
      * **A) To automatically retry failed invocations**: Retries are configured separately.
      * **C) To increase function concurrency**: CloudWatch Logs does not affect concurrency.
      * **D) To extend the execution timeout**: CloudWatch Logs does not affect timeout.
19. **How can environment variables be used securely in Lambda functions?**

    * A) By using IAM roles to encrypt them
    * B) By storing them in plain text
    * C) By using AWS KMS to encrypt sensitive data
    * D) By configuring them in the function code

    **Answer: C) By using AWS KMS to encrypt sensitive data**

    * **Explanation**: AWS KMS can be used to encrypt sensitive data stored in environment variables.
    * **Incorrect Options**:
      * **A) By using IAM roles to encrypt them**: IAM roles do not encrypt environment variables.
      * **B) By storing them in plain text**: Not secure.
      * **D) By configuring them in the function code**: Does not secure the variables.
20. **What is the default limit for Lambda function execution duration?**

    * A) 1 minute
    * B) 3 minutes
    * C) 5 minutes
    * D) 15 minutes

    **Answer: D) 15 minutes**

    * **Explanation**: The default limit for Lambda function execution duration is 15 minutes.
    * **Incorrect Options**:
      * **A) 1 minute**: Incorrect duration.
      * **B) 3 minutes**: Incorrect duration.
      * **C) 5 minutes**: Incorrect duration.

#### Integration with Other AWS Services

21. **Which service is used to expose HTTP endpoints that trigger Lambda functions?**

    * A) Amazon S3
    * B) AWS Glue
    * C) AWS Data Pipeline
    * D) API Gateway

    **Answer: D) API Gateway**

    * **Explanation**: API Gateway is used to expose HTTP endpoints that can trigger Lambda functions.
    * **Incorrect Options**:
      * **A) Amazon S3**: Primarily for object storage.
      * **B) AWS Glue**: Primarily for ETL processes.
      * **C) AWS Data Pipeline**: For data workflows, not for exposing HTTP endpoints.
22. **Which authorization method can be used with API Gateway to secure access to Lambda functions?**

    * A) AWS KMS
    * B) IAM roles
    * C) CloudFront
    * D) EC2 security groups

    **Answer: B) IAM roles**

    * **Explanation**: IAM roles can be used with API Gateway to secure access to Lambda functions.
    * **Incorrect Options**:
      * **A) AWS KMS**: Used for encryption, not authorization.
      * **C) CloudFront**: A CDN service, not used for securing Lambda functions.
      * **D) EC2 security groups**: Used for network security, not for securing Lambda functions.
23. **Which S3 event can be used to trigger a Lambda function?**

    * A) Object deletion
    * B) Bucket creation
    * C) Object lifecycle expiration
    * D) Access control policy update

    **Answer: A) Object deletion**

    * **Explanation**: Lambda functions can be triggered by S3 events such as object creation, deletion, or modification.
    * **Incorrect Options**:
      * **B) Bucket creation**: Does not trigger Lambda functions.
      * **C) Object lifecycle expiration**: Does not trigger Lambda functions.
      * **D) Access control policy update**: Does not trigger Lambda functions.
24. **How can Lambda functions be used with DynamoDB Streams?**

    * A) To delete old records
    * B) To handle data modifications in real-time
    * C) To increase storage capacity
    * D) To backup data automatically

    **Answer: B) To handle data modifications in real-time**

    * **Explanation**: Lambda functions can process DynamoDB Streams to handle data modifications in real-time.
    * **Incorrect Options**:
      * **A) To delete old records**: Not the primary use case for DynamoDB Streams.
      * **C) To increase storage capacity**: Streams do not affect storage capacity.
      * **D) To backup data automatically**: Streams are not used for automatic backups.
25. **What is the benefit of using SQS with Lambda?**

    * A) To increase memory allocation
    * B) To decouple services and ensure scalability
    * C) To reduce execution timeout
    * D) To manage environment variables

    **Answer: B) To decouple services and ensure scalability**

    * **Explanation**: Using SQS with Lambda helps in decoupling services and ensuring scalability.
    * **Incorrect Options**:
      * **A) To increase memory allocation**: SQS does not affect memory allocation.
      * **C) To reduce execution timeout**: SQS does not affect execution timeout.
      * **D) To manage environment variables**: SQS is not used for managing environment variables.
26. **What can Lambda functions do with data from Amazon Kinesis?**

    * A) Store it directly to Glacier
    * B) Process it in real-time for analytics
    * C) Backup it to an EBS volume
    * D) Encrypt it using CloudHSM

    **Answer: B) Process it in real-time for analytics**

    * **Explanation**: Lambda functions can process real-time data streams from Kinesis for analytics.
    * **Incorrect Options**:
      * **A) Store it directly to Glacier**: Glacier is for long-term archival storage.
      * **C) Backup it to an EBS volume**: Kinesis is not typically used for backups.
      * **D) Encrypt it using CloudHSM**: Encryption is not the primary function of Kinesis.
27. **Which AWS service helps manage the lifecycle of serverless applications?**

    * A) AWS CodeDeploy
    * B) AWS CloudFormation
    * C) AWS CodeBuild
    * D) AWS Elastic Beanstalk

    **Answer: B) AWS CloudFormation**

    * **Explanation**: AWS CloudFormation helps manage the lifecycle of serverless applications by defining infrastructure as code.
    * **Incorrect Options**:
      * **A) AWS CodeDeploy**: Used for deployment automation.
      * **C) AWS CodeBuild**: Used for building code.
      * **D) AWS Elastic Beanstalk**: Used for deploying and scaling web applications and services.
28. **How does API Gateway authorize requests before invoking a Lambda function?**

    * A) By verifying IAM roles, Cognito tokens, or custom authorizers
    * B) By encrypting the request data
    * C) By allocating more memory to the function
    * D) By increasing the function's timeout

    **Answer: A) By verifying IAM roles, Cognito tokens, or custom authorizers**

    * **Explanation**: API Gateway can handle authorization by verifying IAM roles, Cognito tokens, or custom authorizers.
    * **Incorrect Options**:
      * **B) By encrypting the request data**: Encryption is not used for authorization.
      * **C) By allocating more memory to the function**: Memory allocation is managed separately.
      * **D) By increasing the function's timeout**: Timeout settings are managed separately.
29. **What is the primary use case for Lambda functions triggered by S3 events?**

    * A) Data warehousing
    * B) Image processing
    * C) Network monitoring
    * D) System backups

    **Answer: B) Image processing**

    * **Explanation**: Common use cases for Lambda functions triggered by S3 events include image processing.
    * **Incorrect Options**:
      * **A) Data warehousing**: Typically involves more complex data operations.
      * **C) Network monitoring**: Not a primary use case for S3-triggered Lambda functions.
      * **D) System backups**: S3 events are not primarily used for system backups.
30. **Which service is commonly used with Lambda for decoupling and scaling applications?**

    * A) Amazon RDS
    * B) AWS CloudTrail
    * C) Amazon SQS
    * D) AWS CloudHSM

    **Answer: C) Amazon SQS**

    * **Explanation**: Amazon SQS is used for decoupling services and ensuring scalability in applications that use Lambda.
    * **Incorrect Options**:
      * **A) Amazon RDS**: A relational database service.
      * **B) AWS CloudTrail**: Used for logging and monitoring API calls.
      * **D) AWS CloudHSM**: Used for hardware security module encryption.
31. **How does Lambda handle data modifications in DynamoDB streams?**

    * A) By creating a backup
    * B) By sending an SNS notification
    * C) By processing the stream in real-time
    * D) By terminating the function

    **Answer: C) By processing the stream in real-time**

    * **Explanation**: Lambda processes DynamoDB streams in real-time to handle data modifications.
    * **Incorrect Options**:
      * **A) By creating a backup**: Streams are not used for backups.
      * **B) By sending an SNS notification**: SNS notifications are not the primary function of streams.
      * **D) By terminating the function**: Streams do not terminate functions.
32. **What benefit does using SNS with Lambda provide?**

    * A) Increases function memory
    * B) Enables asynchronous processing of messages
    * C) Reduces function timeout
    * D) Automatically scales EC2 instances

    **Answer: B) Enables asynchronous processing of messages**

    * **Explanation**: Using SNS with Lambda enables asynchronous processing of messages.
    * **Incorrect Options**:
      * **A) Increases function memory**: SNS does not affect memory.
      * **C) Reduces function timeout**: SNS does not affect timeout.
      * **D) Automatically scales EC2 instances**: SNS is not used for scaling EC2 instances.
33. **Which AWS service is used to create RESTful APIs that trigger Lambda functions?**

    * A) AWS Step Functions
    * B) Amazon S3
    * C) API Gateway
    * D) AWS Glue

    **Answer: C) API Gateway**

    * **Explanation**: API Gateway is used to create RESTful APIs that can trigger Lambda functions.
    * **Incorrect Options**:
      * **A) AWS Step Functions**: Used for orchestrating workflows.
      * **B) Amazon S3**: Primarily for object storage.
      * **D) AWS Glue**: Used for ETL processes.
34. **What is the purpose of using provisioned concurrency with Lambda?**

    * A) To ensure a specific number of instances are always ready to respond instantly
    * B) To increase the memory allocation
    * C) To reduce the function's execution timeout
    * D) To improve logging capabilities

    **Answer: A) To ensure a specific number of instances are always ready to respond instantly**

    * **Explanation**: Provisioned concurrency ensures that a specific number of instances are initialized and ready to respond instantly.
    * **Incorrect Options**:
      * **B) To increase the memory allocation**: Memory allocation is managed separately.
      * **C) To reduce the function's execution timeout**: Timeout settings are managed separately.
      * **D) To improve logging capabilities**: Provisioned concurrency does not affect logging.
35. **Which service can Lambda functions use for tracing and analyzing request paths to troubleshoot performance issues?**

    * A) AWS CloudTrail
    * B) AWS X-Ray
    * C) Amazon CloudWatch
    * D) AWS Trusted Advisor

    **Answer: B) AWS X-Ray**

    * **Explanation**: AWS X-Ray is used for tracing and analyzing request paths to troubleshoot performance issues in Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CloudTrail**: Used for logging API calls.
      * **C) Amazon CloudWatch**: Used for monitoring and logging.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
36. **How can Lambda functions securely store sensitive information like database credentials?**

    * A) By using plaintext environment variables
    * B) By using AWS KMS to encrypt environment variables
    * C) By hardcoding them in the function code
    * D) By storing them in a public S3 bucket

    **Answer: B) By using AWS KMS to encrypt environment variables**

    * **Explanation**: AWS KMS can be used to encrypt sensitive data stored in environment variables for Lambda functions.
    * **Incorrect Options**:
      * **A) By using plaintext environment variables**: Not secure.
      * **C) By hardcoding them in the function code**: Not secure.
      * **D) By storing them in a public S3 bucket**: Not secure.
37. **What is a common use case for Lambda functions triggered by DynamoDB Streams?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: A common use case for Lambda functions triggered by DynamoDB Streams is real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not typically related to DynamoDB Streams.
      * **C) Network monitoring**: Not typically related to DynamoDB Streams.
      * **D) System backups**: Not typically related to DynamoDB Streams.
38. **How can Lambda functions handle errors within the code?**

    * A) By using try-catch blocks and logging errors to CloudWatch Logs
    * B) By increasing the function's memory allocation
    * C) By reducing the function's timeout
    * D) By creating more instances

    **Answer: A) By using try-catch blocks and logging errors to CloudWatch Logs**

    * **Explanation**: Lambda functions can handle errors within the code using try-catch blocks and logging errors to CloudWatch Logs.
    * **Incorrect Options**:
      * **B) By increasing the function's memory allocation**: Does not handle errors.
      * **C) By reducing the function's timeout**: Does not handle errors.
      * **D) By creating more instances**: Does not handle errors.
39. **Which AWS service allows you to create and manage infrastructure as code, including Lambda functions?**

    * A) AWS CodePipeline
    * B) AWS CloudFormation
    * C) Amazon RDS
    * D) AWS Trusted Advisor

    **Answer: B) AWS CloudFormation**

    * **Explanation**: AWS CloudFormation allows you to create and manage infrastructure as code, including Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CodePipeline**: Used for continuous delivery.
      * **C) Amazon RDS**: A relational database service.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
40. **Which feature of Lambda allows you to package libraries, custom runtimes, or other dependencies separately?**

    * A) Layers
    * B) Reserved concurrency
    * C) Environment variables
    * D) Provisioned concurrency

    **Answer: A) Layers**

    * **Explanation**: Lambda Layers allow you to package libraries, custom runtimes, or other dependencies separately.
    * **Incorrect Options**:
      * **B) Reserved concurrency**: Limits the maximum number of concurrent executions.
      * **C) Environment variables**: Used to store configuration settings.
      * **D) Provisioned concurrency**: Ensures a specific number of instances are ready to respond instantly.

#### Best Practices

41. **What is the benefit of optimizing memory allocation for Lambda functions?**

    * A) Reduces the function's concurrency limit
    * B) Increases execution time
    * C) Reduces execution time and potentially lowers costs
    * D) Increases the function's timeout

    **Answer: C) Reduces execution time and potentially lowers costs**

    * **Explanation**: Optimizing memory allocation increases CPU power, reducing execution time and potentially lowering costs.
    * **Incorrect Options**:
      * **A) Reduces the function's concurrency limit**: Memory allocation does not affect concurrency.
      * **B) Increases execution time**: Optimizing memory allocation reduces execution time.
      * **D) Increases the function's timeout**: Memory allocation does not affect timeout.
42. **Why is it important to write efficient and minimal code for Lambda functions?**

    * A) To increase function memory
    * B) To improve performance and reduce execution duration
    * C) To ensure the function runs indefinitely
    * D) To automatically scale EC2 instances

    **Answer: B) To improve performance and reduce execution duration**

    * **Explanation**: Writing efficient and minimal code improves performance and reduces execution duration for Lambda functions.
    * **Incorrect Options**:
      * **A) To increase function memory**: Code efficiency does not affect memory.
      * **C) To ensure the function runs indefinitely**: Lambda functions have a maximum execution time of 15 minutes.
      * **D) To automatically scale EC2 instances**: Code efficiency does not affect EC2 scaling.
43. **How can you minimize cold starts for Lambda functions with predictable traffic?**

    * A) By increasing memory allocation
    * B) By using provisioned concurrency
    * C) By reducing the function's timeout
    * D) By using environment variables

    **Answer: B) By using provisioned concurrency**

    * **Explanation**: Provisioned concurrency ensures that instances of the function are pre-initialized, reducing cold starts for predictable traffic.
    * **Incorrect Options**:
      * **A) By increasing memory allocation**: Does not directly affect cold starts.
      * **C) By reducing the function's timeout**: Does not directly affect cold starts.
      * **D) By using environment variables**: Does not directly affect cold starts.
44. **What principle should be followed when assigning permissions to Lambda execution roles?**

    * A) Principle of Least Privilege
    * B) Principle of Maximum Privilege
    * C) Principle of No Privilege
    * D) Principle of Unlimited Privilege

    **Answer: A) Principle of Least Privilege**

    * **Explanation**: Assign the minimal required permissions to Lambda execution roles following the Principle of Least Privilege.
    * **Incorrect Options**:
      * **B) Principle of Maximum Privilege**: Provides unnecessary access.
      * **C) Principle of No Privilege**: Does not provide needed access.
      * **D) Principle of Unlimited Privilege**: Provides unnecessary access.
45. **How can sensitive data stored in environment variables be protected in Lambda functions?**

    * A) By using plaintext
    * B) By encrypting them with AWS KMS
    * C) By hardcoding them in the function code
    * D) By storing them in a public S3 bucket

    **Answer: B) By encrypting them with AWS KMS**

    * **Explanation**: Sensitive data in environment variables should be encrypted with AWS KMS for protection.
    * **Incorrect Options**:
      * **A) By using plaintext**: Not secure.
      * **C) By hardcoding them in the function code**: Not secure.
      * **D) By storing them in a public S3 bucket**: Not secure.
46. **Why is monitoring and analyzing Lambda usage important for cost management?**

    * A) To increase memory allocation
    * B) To extend the execution timeout
    * C) To optimize function logic and reduce execution time and costs
    * D) To manage environment variables

    **Answer: C) To optimize function logic and reduce execution time and costs**

    * **Explanation**: Monitoring and analyzing usage helps optimize function logic and reduce execution time and costs.
    * **Incorrect Options**:
      * **A) To increase memory allocation**: Monitoring does not affect memory allocation.
      * **B) To extend the execution timeout**: Monitoring does not affect timeout.
      * **D) To manage environment variables**: Monitoring does not manage environment variables.
47. **How can unnecessary Lambda invocations be minimized to reduce costs?**

    * A) By increasing function memory
    * B) By using provisioned concurrency
    * C) By implementing a filtering mechanism for events
    * D) By increasing the function's timeout

    **Answer: C) By implementing a filtering mechanism for events**

    * **Explanation**: Implementing a filtering mechanism ensures only relevant events trigger Lambda functions, minimizing unnecessary invocations and reducing costs.
    * **Incorrect Options**:
      * **A) By increasing function memory**: Does not affect invocations.
      * **B) By using provisioned concurrency**: Does not affect invocations.
      * **D) By increasing the function's timeout**: Does not affect invocations.
48. **What is a common scenario for using Lambda with Amazon Kinesis?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: Lambda functions are commonly used with Amazon Kinesis for real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not a primary use case for Kinesis.
      * **C) Network monitoring**: Not a primary use case for Kinesis.
      * **D) System backups**: Not a primary use case for Kinesis.
49. **What is the main advantage of using AWS Lambda for serverless web applications?**

    * A) It provides unlimited execution time
    * B) It automatically manages server infrastructure
    * C) It requires manual scaling
    * D) It increases network traffic

    **Answer: B) It automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) It provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) It requires manual scaling**: Lambda scales automatically.
      * **D) It increases network traffic**: Lambda does not inherently increase network traffic.
50. **Which AWS service can be used to create RESTful APIs that trigger Lambda functions?**

    * A) AWS Step Functions
    * B) Amazon S3
    * C) API Gateway
    * D) AWS Glue

    **Answer: C) API Gateway**

    * **Explanation**: API Gateway is used to create RESTful APIs that can trigger Lambda functions.
    * **Incorrect Options**:
      * **A) AWS Step Functions**: Used for orchestrating workflows.
      * **B) Amazon S3**: Primarily for object storage.
      * **D) AWS Glue**: Used for ETL processes.

#### Advanced Scenarios

51. **How can Lambda handle the automatic scaling of a function when processing a stream of data from Amazon Kinesis?**

    * A) By using fixed concurrency
    * B) By specifying a maximum execution time
    * C) By processing data in real-time and adjusting the concurrency based on the stream's shard count
    * D) By manually adjusting memory settings

    **Answer: C) By processing data in real-time and adjusting the concurrency based on the stream's shard count**

    * **Explanation**: Lambda scales automatically based on the number of shards in a Kinesis stream.
    * **Incorrect Options**:
      * **A) By using fixed concurrency**: Does not adjust based on data stream.
      * **B) By specifying a maximum execution time**: Execution time does not affect scaling.
      * **D) By manually adjusting memory settings**: Memory settings do not control scaling.
52. **Which feature allows Lambda functions to share common code or libraries without duplicating them in each function deployment package?**

    * A) Provisioned concurrency
    * B) Layers
    * C) Reserved concurrency
    * D) Environment variables

    **Answer: B) Layers**

    * **Explanation**: Layers allow Lambda functions to share common code or libraries.
    * **Incorrect Options**:
      * **A) Provisioned concurrency**: Ensures readiness of function instances.
      * **C) Reserved concurrency**: Limits concurrent executions.
      * **D) Environment variables**: Used for storing configuration settings.
53. **What does setting the reserved concurrency for a Lambda function do?**

    * A) Ensures the function runs faster
    * B) Limits the maximum number of concurrent executions
    * C) Allocates more memory to the function
    * D) Triggers the function more frequently

    **Answer: B) Limits the maximum number of concurrent executions**

    * **Explanation**: Reserved concurrency limits the number of concurrent executions to ensure other functions have resources.
    * **Incorrect Options**:
      * **A) Ensures the function runs faster**: Concurrency does not affect execution speed.
      * **C) Allocates more memory to the function**: Memory allocation is separate from concurrency settings.
      * **D) Triggers the function more frequently**: Concurrency settings do not affect trigger frequency.
54. **Which service allows for orchestration of Lambda functions into complex workflows?**

    * A) Amazon S3
    * B) AWS Glue
    * C) AWS Step Functions
    * D) Amazon RDS

    **Answer: C) AWS Step Functions**

    * **Explanation**: AWS Step Functions allow for orchestration of Lambda functions into complex workflows.
    * **Incorrect Options**:
      * **A) Amazon S3**: Primarily for object storage.
      * **B) AWS Glue**: Primarily for ETL processes.
      * **D) Amazon RDS**: Relational database service.
55. **What is the main use of Lambda Layers?**

    * A) To increase function memory
    * B) To package and share libraries and dependencies
    * C) To extend the execution timeout
    * D) To manage environment variables

    **Answer: B) To package and share libraries and dependencies**

    * **Explanation**: Lambda Layers are used to package and share libraries and dependencies.
    * **Incorrect Options**:
      * **A) To increase function memory**: Layers do not affect memory allocation.
      * **C) To extend the execution timeout**: Layers do not affect timeout settings.
      * **D) To manage environment variables**: Environment variables are managed separately.
56. **What is a common use case for integrating Lambda with Amazon SNS?**

    * A) Data warehousing
    * B) Sending notifications and alerts
    * C) Network monitoring
    * D) System backups

    **Answer: B) Sending notifications and alerts**

    * **Explanation**: A common use case for integrating Lambda with Amazon SNS is sending notifications and alerts.
    * **Incorrect Options**:
      * **A) Data warehousing**: Not typically related to SNS.
      * **C) Network monitoring**: Not typically related to SNS.
      * **D) System backups**: Not typically related to SNS.
57. **What is the main advantage of using AWS Lambda for a serverless application?**

    * A) Provides unlimited execution time
    * B) Automatically manages server infrastructure
    * C) Requires manual scaling
    * D) Increases network traffic

    **Answer: B) Automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) Provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) Requires manual scaling**: Lambda scales automatically.
      * **D) Increases network traffic**: Lambda does not inherently increase network traffic.
58. **How can Lambda functions be secured when accessing sensitive data?**

    * A) By using IAM roles
    * B) By encrypting data with AWS KMS
    * C) By using plaintext environment variables
    * D) By hardcoding sensitive data in the function code

    **Answer: B) By encrypting data with AWS KMS**

    * **Explanation**: Sensitive data should be encrypted with AWS KMS for security.
    * **Incorrect Options**:
      * **A) By using IAM roles**: IAM roles provide access control, not encryption.
      * **C) By using plaintext environment variables**: Not secure.
      * **D) By hardcoding sensitive data in the function code**: Not secure.
59. **What is the benefit of using AWS Lambda with Amazon DynamoDB Streams?**

    * A) To increase storage capacity
    * B) To process real-time data changes
    * C) To backup data automatically
    * D) To manage environment variables

    **Answer: B) To process real-time data changes**

    * **Explanation**: AWS Lambda can process real-time data changes with DynamoDB Streams.
    * **Incorrect Options**:
      * **A) To increase storage capacity**: Streams do not affect storage capacity.
      * **C) To backup data automatically**: Streams are not used for backups.
      * **D) To manage environment variables**: Streams are not used for managing environment variables.
60. **Which AWS service helps manage and deploy serverless applications as a single unit?**

    * A) AWS CodePipeline
    * B) AWS SAM (Serverless Application Model)
    * C) AWS CloudFormation
    * D) Amazon RDS

    **Answer: B) AWS SAM (Serverless Application Model)**

    * **Explanation**: AWS SAM helps manage and deploy serverless applications as a single unit.
    * **Incorrect Options**:
      * **A) AWS CodePipeline**: Used for continuous delivery.
      * **C) AWS CloudFormation**: Used for infrastructure as code, but SAM specifically for serverless applications.
      * **D) Amazon RDS**: Relational database service.
61. **How does Lambda handle scaling for functions processing data from Amazon Kinesis streams?**

    * A) By using fixed concurrency
    * B) By processing data in real-time and adjusting concurrency based on the stream's shard count
    * C) By specifying a maximum execution time
    * D) By manually adjusting memory settings

    **Answer: B) By processing data in real-time and adjusting concurrency based on the stream's shard count**

    * **Explanation**: Lambda scales automatically based on the number of shards in a Kinesis stream.
    * **Incorrect Options**:
      * **A) By using fixed concurrency**: Does not adjust based on data stream.
      * **C) By specifying a maximum execution time**: Execution time does not affect scaling.
      * **D) By manually adjusting memory settings**: Memory settings do not control scaling.
62. **Which feature allows Lambda functions to share common code or libraries without duplicating them in each function deployment package?**

    * A) Provisioned concurrency
    * B) Layers
    * C) Reserved concurrency
    * D) Environment variables

    **Answer: B) Layers**

    * **Explanation**: Layers allow Lambda functions to share common code or libraries.
    * **Incorrect Options**:
      * **A) Provisioned concurrency**: Ensures readiness of function instances.
      * **C) Reserved concurrency**: Limits concurrent executions.
      * **D) Environment variables**: Used for storing configuration settings.
63. **Which feature allows you to package libraries and dependencies separately for Lambda functions?**

    * A) Provisioned concurrency
    * B) Layers
    * C) Reserved concurrency
    * D) Environment variables

    **Answer: B) Layers**

    * **Explanation**: Layers allow you to package libraries and dependencies separately for Lambda functions.
    * **Incorrect Options**:
      * **A) Provisioned concurrency**: Ensures readiness of function instances.
      * **C) Reserved concurrency**: Limits concurrent executions.
      * **D) Environment variables**: Used for storing configuration settings.
64. **How does Lambda handle scaling for functions processing data from Amazon Kinesis streams?**

    * A) By using fixed concurrency
    * B) By processing data in real-time and adjusting concurrency based on the stream's shard count
    * C) By specifying a maximum execution time
    * D) By manually adjusting memory settings

    **Answer: B) By processing data in real-time and adjusting concurrency based on the stream's shard count**

    * **Explanation**: Lambda scales automatically based on the number of shards in a Kinesis stream.
    * **Incorrect Options**:
      * **A) By using fixed concurrency**: Does not adjust based on data stream.
      * **C) By specifying a maximum execution time**: Execution time does not affect scaling.
      * **D) By manually adjusting memory settings**: Memory settings do not control scaling.
65. **What is the main use of Lambda Layers?**

    * A) To increase function memory
    * B) To package and share libraries and dependencies
    * C) To extend the execution timeout
    * D) To manage environment variables

    **Answer: B) To package and share libraries and dependencies**

    * **Explanation**: Lambda Layers are used to package and share libraries and dependencies.
    * **Incorrect Options**:
      * **A) To increase function memory**: Layers do not affect memory allocation.
      * **C) To extend the execution timeout**: Layers do not affect timeout settings.
      * **D) To manage environment variables**: Environment variables are managed separately.
66. **Which AWS service can be used to create and manage RESTful APIs that trigger Lambda functions?**

    * A) AWS Step Functions
    * B) Amazon S3
    * C) API Gateway
    * D) AWS Glue

    **Answer: C) API Gateway**

    * **Explanation**: API Gateway is used to create and manage RESTful APIs that trigger Lambda functions.
    * **Incorrect Options**:
      * **A) AWS Step Functions**: Used for orchestrating workflows.
      * **B) Amazon S3**: Primarily for object storage.
      * **D) AWS Glue**: Used for ETL processes.
67. **How can Lambda functions securely store sensitive information like database credentials?**

    * A) By using plaintext environment variables
    * B) By using AWS KMS to encrypt environment variables
    * C) By hardcoding them in the function code
    * D) By storing them in a public S3 bucket

    **Answer: B) By using AWS KMS to encrypt environment variables**

    * **Explanation**: AWS KMS can be used to encrypt sensitive data stored in environment variables for Lambda functions.
    * **Incorrect Options**:
      * **A) By using plaintext environment variables**: Not secure.
      * **C) By hardcoding them in the function code**: Not secure.
      * **D) By storing them in a public S3 bucket**: Not secure.
68. **What is the primary use case for Lambda functions triggered by S3 events?**

    * A) Data warehousing
    * B) Image processing
    * C) Network monitoring
    * D) System backups

    **Answer: B) Image processing**

    * **Explanation**: Common use cases for Lambda functions triggered by S3 events include image processing.
    * **Incorrect Options**:
      * **A) Data warehousing**: Typically involves more complex data operations.
      * **C) Network monitoring**: Not a primary use case for S3-triggered Lambda functions.
      * **D) System backups**: S3 events are not primarily used for system backups.
69. **What is a common scenario for using Lambda with Amazon Kinesis?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: Lambda functions are commonly used with Amazon Kinesis for real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not a primary use case for Kinesis.
      * **C) Network monitoring**: Not a primary use case for Kinesis.
      * **D) System backups**: Not a primary use case for Kinesis.
70. **What is the main benefit of using AWS Lambda for serverless web applications?**

    * A) It provides unlimited execution time
    * B) It automatically manages server infrastructure
    * C) It requires manual scaling
    * D) It increases network traffic

    **Answer: B) It automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) It provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) It requires manual scaling**: Lambda scales automatically.
      * **D) It increases network traffic**: Lambda does not inherently increase network traffic.
71. **Which AWS service can Lambda functions use for tracing and analyzing request paths to troubleshoot performance issues?**

    * A) AWS CloudTrail
    * B) AWS X-Ray
    * C) Amazon CloudWatch
    * D) AWS Trusted Advisor

    **Answer: B) AWS X-Ray**

    * **Explanation**: AWS X-Ray is used for tracing and analyzing request paths to troubleshoot performance issues in Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CloudTrail**: Used for logging API calls.
      * **C) Amazon CloudWatch**: Used for monitoring and logging.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
72. **What does setting the reserved concurrency for a Lambda function do?**

    * A) Ensures the function runs faster
    * B) Limits the maximum number of concurrent executions
    * C) Allocates more memory to the function
    * D) Triggers the function more frequently

    **Answer: B) Limits the maximum number of concurrent executions**

    * **Explanation**: Reserved concurrency limits the number of concurrent executions to ensure other functions have resources.
    * **Incorrect Options**:
      * **A) Ensures the function runs faster**: Concurrency does not affect execution speed.
      * **C) Allocates more memory to the function**: Memory allocation is separate from concurrency settings.
      * **D) Triggers the function more frequently**: Concurrency settings do not affect trigger frequency.
73. **Which service allows for orchestration of Lambda functions into complex workflows?**

    * A) Amazon S3
    * B) AWS Glue
    * C) AWS Step Functions
    * D) Amazon RDS

    **Answer: C) AWS Step Functions**

    * **Explanation**: AWS Step Functions allow for orchestration of Lambda functions into complex workflows.
    * **Incorrect Options**:
      * **A) Amazon S3**: Primarily for object storage.
      * **B) AWS Glue**: Primarily for ETL processes.
      * **D) Amazon RDS**: Relational database service.
74. **How can Lambda functions be secured when accessing sensitive data?**

    * A) By using IAM roles
    * B) By encrypting data with AWS KMS
    * C) By using plaintext environment variables
    * D) By hardcoding sensitive data in the function code

    **Answer: B) By encrypting data with AWS KMS**

    * **Explanation**: Sensitive data should be encrypted with AWS KMS for security.
    * **Incorrect Options**:
      * **A) By using IAM roles**: IAM roles provide access control, not encryption.
      * **C) By using plaintext environment variables**: Not secure.
      * **D) By hardcoding sensitive data in the function code**: Not secure.
75. **What is a common use case for Lambda functions triggered by DynamoDB Streams?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: A common use case for Lambda functions triggered by DynamoDB Streams is real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not typically related to DynamoDB Streams.
      * **C) Network monitoring**: Not typically related to DynamoDB Streams.
      * **D) System backups**: Not typically related to DynamoDB Streams.
76. **What is the primary use case for Lambda functions triggered by S3 events?**

    * A) Data warehousing
    * B) Image processing
    * C) Network monitoring
    * D) System backups

    **Answer: B) Image processing**

    * **Explanation**: Common use cases for Lambda functions triggered by S3 events include image processing.
    * **Incorrect Options**:
      * **A) Data warehousing**: Typically involves more complex data operations.
      * **C) Network monitoring**: Not a primary use case for S3-triggered Lambda functions.
      * **D) System backups**: S3 events are not primarily used for system backups.
77. **What is a common scenario for using Lambda with Amazon Kinesis?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: Lambda functions are commonly used with Amazon Kinesis for real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not a primary use case for Kinesis.
      * **C) Network monitoring**: Not a primary use case for Kinesis.
      * **D) System backups**: Not a primary use case for Kinesis.
78. **What is the main benefit of using AWS Lambda for serverless web applications?**

    * A) It provides unlimited execution time
    * B) It automatically manages server infrastructure
    * C) It requires manual scaling
    * D) It increases network traffic

    **Answer: B) It automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) It provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) It requires manual scaling**: Lambda scales automatically.
      * **D) It increases network traffic**: Lambda does not inherently increase network traffic.
79. **What is the main advantage of using AWS Lambda for a serverless application?**

    * A) Provides unlimited execution time
    * B) Automatically manages server infrastructure
    * C) Requires manual scaling
    * D) Increases network traffic

    **Answer: B) Automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) Provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) Requires manual scaling**: Lambda scales automatically.
      * **D) Increases network traffic**: Lambda does not inherently increase network traffic.
80. **Which AWS service can Lambda functions use for tracing and analyzing request paths to troubleshoot performance issues?**

    * A) AWS CloudTrail
    * B) AWS X-Ray
    * C) Amazon CloudWatch
    * D) AWS Trusted Advisor

    **Answer: B) AWS X-Ray**

    * **Explanation**: AWS X-Ray is used for tracing and analyzing request paths to troubleshoot performance issues in Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CloudTrail**: Used for logging API calls.
      * **C) Amazon CloudWatch**: Used for monitoring and logging.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
81. **How can Lambda functions handle errors within the code?**

    * A) By using try-catch blocks and logging errors to CloudWatch Logs
    * B) By increasing the function's memory allocation
    * C) By reducing the function's timeout
    * D) By creating more instances

    **Answer: A) By using try-catch blocks and logging errors to CloudWatch Logs**

    * **Explanation**: Lambda functions can handle errors within the code using try-catch blocks and logging errors to CloudWatch Logs.
    * **Incorrect Options**:
      * **B) By increasing the function's memory allocation**: Does not handle errors.
      * **C) By reducing the function's timeout**: Does not handle errors.
      * **D) By creating more instances**: Does not handle errors.
82. **Which AWS service allows you to create and manage infrastructure as code, including Lambda functions?**

    * A) AWS CodePipeline
    * B) AWS CloudFormation
    * C) Amazon RDS
    * D) AWS Trusted Advisor

    **Answer: B) AWS CloudFormation**

    * **Explanation**: AWS CloudFormation allows you to create and manage infrastructure as code, including Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CodePipeline**: Used for continuous delivery.
      * **C) Amazon RDS**: A relational database service.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
83. **Which feature of Lambda allows you to package libraries, custom runtimes, or other dependencies separately?**

    * A) Layers
    * B) Reserved concurrency
    * C) Environment variables
    * D) Provisioned concurrency

    **Answer: A) Layers**

    * **Explanation**: Lambda Layers allow you to package libraries, custom runtimes, or other dependencies separately.
    * **Incorrect Options**:
      * **B) Reserved concurrency**: Limits the maximum number of concurrent executions.
      * **C) Environment variables**: Used to store configuration settings.
      * **D) Provisioned concurrency**: Ensures a specific number of instances are ready to respond instantly.
84. **Which service is commonly used with Lambda for decoupling and scaling applications?**

    * A) Amazon RDS
    * B) AWS CloudTrail
    * C) Amazon SQS
    * D) AWS CloudHSM

    **Answer: C) Amazon SQS**

    * **Explanation**: Amazon SQS is used for decoupling services and ensuring scalability in applications that use Lambda.
    * **Incorrect Options**:
      * **A) Amazon RDS**: A relational database service.
      * **B) AWS CloudTrail**: Used for logging and monitoring API calls.
      * **D) AWS CloudHSM**: Used for hardware security module encryption.
85. **How does Lambda handle data modifications in DynamoDB streams?**

    * A) By creating a backup
    * B) By sending an SNS notification
    * C) By processing the stream in real-time
    * D) By terminating the function

    **Answer: C) By processing the stream in real-time**

    * **Explanation**: Lambda processes DynamoDB streams in real-time to handle data modifications.
    * **Incorrect Options**:
      * **A) By creating a backup**: Streams are not used for backups.
      * **B) By sending an SNS notification**: SNS notifications are not the primary function of streams.
      * **D) By terminating the function**: Streams do not terminate functions.
86. **What benefit does using SNS with Lambda provide?**

    * A) Increases function memory
    * B) Enables asynchronous processing of messages
    * C) Reduces function timeout
    * D) Automatically scales EC2 instances

    **Answer: B) Enables asynchronous processing of messages**

    * **Explanation**: Using SNS with Lambda enables asynchronous processing of messages.
    * **Incorrect Options**:
      * **A) Increases function memory**: SNS does not affect memory.
      * **C) Reduces function timeout**: SNS does not affect timeout.
      * **D) Automatically scales EC2 instances**: SNS is not used for scaling EC2 instances.
87. **Which AWS service is used to create RESTful APIs that trigger Lambda functions?**

    * A) AWS Step Functions
    * B) Amazon S3
    * C) API Gateway
    * D) AWS Glue

    **Answer: C) API Gateway**

    * **Explanation**: API Gateway is used to create RESTful APIs that can trigger Lambda functions.
    * **Incorrect Options**:
      * **A) AWS Step Functions**: Used for orchestrating workflows.
      * **B) Amazon S3**: Primarily for object storage.
      * **D) AWS Glue**: Used for ETL processes.
88. **Which AWS service can be used to create and manage RESTful APIs that trigger Lambda functions?**

    * A) AWS Step Functions
    * B) Amazon S3
    * C) API Gateway
    * D) AWS Glue

    **Answer: C) API Gateway**

    * **Explanation**: API Gateway is used to create and manage RESTful APIs that trigger Lambda functions.
    * **Incorrect Options**:
      * **A) AWS Step Functions**: Used for orchestrating workflows.
      * **B) Amazon S3**: Primarily for object storage.
      * **D) AWS Glue**: Used for ETL processes.
89. **How can Lambda functions securely store sensitive information like database credentials?**

    * A) By using plaintext environment variables
    * B) By using AWS KMS to encrypt environment variables
    * C) By hardcoding them in the function code
    * D) By storing them in a public S3 bucket

    **Answer: B) By using AWS KMS to encrypt environment variables**

    * **Explanation**: AWS KMS can be used to encrypt sensitive data stored in environment variables for Lambda functions.
    * **Incorrect Options**:
      * **A) By using plaintext environment variables**: Not secure.
      * **C) By hardcoding them in the function code**: Not secure.
      * **D) By storing them in a public S3 bucket**: Not secure.
90. **What is the primary use case for Lambda functions triggered by S3 events?**

    * A) Data warehousing
    * B) Image processing
    * C) Network monitoring
    * D) System backups

    **Answer: B) Image processing**

    * **Explanation**: Common use cases for Lambda functions triggered by S3 events include image processing.
    * **Incorrect Options**:
      * **A) Data warehousing**: Typically involves more complex data operations.
      * **C) Network monitoring**: Not a primary use case for S3-triggered Lambda functions.
      * **D) System backups**: S3 events are not primarily used for system backups.
91. **What is a common scenario for using Lambda with Amazon Kinesis?**

    * A) Image processing
    * B) Real-time data analytics
    * C) Network monitoring
    * D) System backups

    **Answer: B) Real-time data analytics**

    * **Explanation**: Lambda functions are commonly used with Amazon Kinesis for real-time data analytics.
    * **Incorrect Options**:
      * **A) Image processing**: Not a primary use case for Kinesis.
      * **C) Network monitoring**: Not a primary use case for Kinesis.
      * **D) System backups**: Not a primary use case for Kinesis.
92. **What is the main benefit of using AWS Lambda for serverless web applications?**

    * A) It provides unlimited execution time
    * B) It automatically manages server infrastructure
    * C) It requires manual scaling
    * D) It increases network traffic

    **Answer: B) It automatically manages server infrastructure**

    * **Explanation**: AWS Lambda automatically manages the server infrastructure, allowing developers to focus on code.
    * **Incorrect Options**:
      * **A) It provides unlimited execution time**: Lambda functions have a maximum execution time of 15 minutes.
      * **C) It requires manual scaling**: Lambda scales automatically.
      * **D) It increases network traffic**: Lambda does not inherently increase network traffic.
93. **Which AWS service can Lambda functions use for tracing and analyzing request paths to troubleshoot performance issues?**

    * A) AWS CloudTrail
    * B) AWS X-Ray
    * C) Amazon CloudWatch
    * D) AWS Trusted Advisor

    **Answer: B) AWS X-Ray**

    * **Explanation**: AWS X-Ray is used for tracing and analyzing request paths to troubleshoot performance issues in Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CloudTrail**: Used for logging API calls.
      * **C) Amazon CloudWatch**: Used for monitoring and logging.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
94. **How can Lambda functions handle errors within the code?**

    * A) By using try-catch blocks and logging errors to CloudWatch Logs
    * B) By increasing the function's memory allocation
    * C) By reducing the function's timeout
    * D) By creating more instances

    **Answer: A) By using try-catch blocks and logging errors to CloudWatch Logs**

    * **Explanation**: Lambda functions can handle errors within the code using try-catch blocks and logging errors to CloudWatch Logs.
    * **Incorrect Options**:
      * **B) By increasing the function's memory allocation**: Does not handle errors.
      * **C) By reducing the function's timeout**: Does not handle errors.
      * **D) By creating more instances**: Does not handle errors.
95. **Which AWS service allows you to create and manage infrastructure as code, including Lambda functions?**

    * A) AWS CodePipeline
    * B) AWS CloudFormation
    * C) Amazon RDS
    * D) AWS Trusted Advisor

    **Answer: B) AWS CloudFormation**

    * **Explanation**: AWS CloudFormation allows you to create and manage infrastructure as code, including Lambda functions.
    * **Incorrect Options**:
      * **A) AWS CodePipeline**: Used for continuous delivery.
      * **C) Amazon RDS**: A relational database service.
      * **D) AWS Trusted Advisor**: Provides best practice recommendations.
96. **Which feature of Lambda allows you to package libraries, custom runtimes, or other dependencies separately?**

    * A) Layers
    * B) Reserved concurrency
    * C) Environment variables
    * D) Provisioned concurrency

    **Answer: A) Layers**

    * **Explanation**: Lambda Layers allow you to package libraries, custom runtimes, or other dependencies separately.
    * **Incorrect Options**:
      * **B) Reserved concurrency**: Limits the maximum number of concurrent executions.
      * **C) Environment variables**: Used to store configuration settings.
      * **D) Provisioned concurrency**: Ensures a specific number of instances are ready to respond instantly.
97. **Which service is commonly used with Lambda for decoupling and scaling applications?**

    * A) Amazon RDS
    * B) AWS CloudTrail
    * C) Amazon SQS
    * D) AWS CloudHSM

    **Answer: C) Amazon SQS**

    * **Explanation**: Amazon SQS is used for decoupling services and ensuring scalability in applications that use Lambda.
    * **Incorrect Options**:
      * **A) Amazon RDS**: A relational database service.
      * **B) AWS CloudTrail**: Used for logging and monitoring API calls.
      * **D) AWS CloudHSM**: Used for hardware security module encryption.
98. **How does Lambda handle data modifications in DynamoDB streams?**

    * A) By creating a backup
    * B) By sending an SNS notification
    * C) By processing the stream in real-time
    * D) By terminating the function

    **Answer: C) By processing the stream in real-time**

    * **Explanation**: Lambda processes DynamoDB streams in real-time to handle data modifications.
    * **Incorrect Options**:
      * **A) By creating a backup**: Streams are not used for backups.
      * **B) By sending an SNS notification**: SNS notifications are not the primary function of streams.
      * **D) By terminating the function**: Streams do not terminate functions.
99. **What benefit does using SNS with Lambda provide?**

    * A) Increases function memory
    * B) Enables asynchronous processing of messages
    * C) Reduces function timeout
    * D) Automatically scales EC2 instances

    **Answer: B) Enables asynchronous processing of messages**

    * **Explanation**: Using SNS with Lambda enables asynchronous processing of messages.
    * **Incorrect Options**:
      * **A) Increases function memory**: SNS does not affect memory.
      * **C) Reduces function timeout**: SNS does not affect timeout.
      * **D) Automatically scales EC2 instances**: SNS is not used for scaling EC2 instances.
