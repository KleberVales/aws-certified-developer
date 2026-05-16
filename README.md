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

## 2. Segurança 

## 3. Implantação 

## 4. Solução de problemas e otimização 
