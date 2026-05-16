# aws-certified-developer

## 1. Desenvolvimento com os serviços da AWS

### Desenvolver código para aplicações hospedadas na AWS

- Fundamentals of Architecture
  * Architectural patterns: event-driven, microservices, monolithic, choreography vs. orchestration, fanout
  * Stateful vs. Stateless
  * Tight vs. Loose coupling
  * Synchronous vs. Asynchronous
    
- Messaging, Events and Streaming
  * Messaging services: SQS, SNS, EventBridge
  * EventBridge: event-driven patterns
  * Streaming data: Kinesis Data Streams, Kinesis Firehose
 
- APIs, SDKs, and Code Resilience
  * Create and maintain APIs (API Gateway: transformations, validation, status codes)
  * Use AWS SDK and APIs (boto3, AWS SDK for JavaScript, etc.)
  * Resilient and fault-tolerant code
  * Retry logic, circuit breaker, error handling for third-party integrations

 ### Develop code for AWS Lambda

 - AWS Lambda (background and performance)
   * Configuration of functions (memory, timeout, handler, layers, runtime, extensions)
   * Access to private resources in VPC
   * Lifecycle, destinations, DLQ (Dead Letter Queue)
   * Integration with other AWS services
   * Performance tuning (cold start, provisioned concurrency)
   * Real-time data processing

 ### Using data storage in application development

 - Data Storage

| Sub-bloco | Tópicos | 
|-----------|---------|
| DynamoDB | Partition keys, cardinalidade, índices (GSI/LSI), Query vs Scan |
| Consistência | Modelos fortemente vs eventualmente consistentes |
| Ciclo de vida dos dados | S3 Lifecycle, TTL no DynamoDB |
| Cache | ElastiCache (Redis/Memcached), DAX |
| Armazenamentos especializados | OpenSearch Service |
| Serialização | JSON, protobuf, persistência |

## 2. Security

### Implement authentication and/or authorization for AWS applications and services.

- IAM & Identity Fundamentals (start here — everything else depends on this)
  * Configuring programmatic access to AWS (access keys, CLI profiles, instance profiles)
  * Making authenticated calls to AWS services (SigV4 signing)
  * Assuming IAM roles (sts:AssumeRole, role chaining)
  * Defining permissions for IAM principals (policies: identity-based, resource-based, boundaries)

## 3. Implantação 

## 4. Solução de problemas e otimização 

---

https://docs.aws.amazon.com/pt_br/aws-certification/latest/developer-associate-02/developer-associate-02.html?refid=990e3b45-5609-4136-9ce5-fb7c47b9ec52#developer-associate-02-exam-content
