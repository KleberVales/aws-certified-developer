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
 
- Authentication & Authorization for Applications
  * Federated access with Amazon Cognito (User Pools, Identity Pools) and IAM identity providers (SAML, OIDC)
  * Protecting applications using bearer tokens (JWT, OAuth 2.0 flows)
  * Application-level authorization for fine-grained access control (e.g. ABAC, custom authorizers in API Gateway)
  * Service-to-service authentication in microservices architectures (IAM roles, service accounts, mTLS)
 
### Implementing encryption using AWS services

- Encryption

| Sub-block | Topics |
|-----------|---------|
| KMS & Key Management | Encryption at rest vs in transit, client-side vs server-side encryption, using KMS keys to encrypt/decrypt, cross-account encryption, key rotation (enable/disable) |
| Certificates & PKIAWS | Private CA, generating SSL/TLS certificates, generating SSH keys for development |

### Managing sensitive data in application code

- Sensitive Data Management in Code
  * Data classification concepts: PII, PHI, and regulatory implications
  * Encrypting environment variables in Lambda (KMS + SSM Parameter Store)
  * Using AWS Secrets Manager and SSM Parameter Store to protect secrets
  * Sanitizing and masking sensitive data at the application level
  * Multi-tenant data access patterns (row-level security, tenant isolation strategies)

## 3. Deployment

### Prepare application artifacts for deployment on AWS

- Packaging & Artifact Preparation (foundation — study before anything else)
  * Managing code module dependencies: environment variables, config files, container images
  * Directory and file structure for application deployment
  * Using code repositories in deployment environments (CodeCommit, GitHub)
  * Matching application requirements to resources (memory, CPU/cores)
  * Environment-specific configurations using AWS AppConfig (feature flags, config profiles)
 
💡 This block is about getting your artifact ready before it ever touches a pipeline. AppConfig is frequently tested — know the difference between a configuration profile and a deployment strategy.

### Testing applications in development environments

- Testing in Development Environments
  * Testing deployed code using AWS tools (SAM CLI sam local invoke, sam local start-api)
  * Writing integration tests and mocking external API dependencies
  * Testing via API Gateway development endpoints and stage configurations
  * Deploying application stack updates to existing environments (e.g. SAM deploy to staging)
  * Testing event-driven applications (simulating SQS, SNS, EventBridge payloads)

💡 Heavily tied to Domain 1 (Lambda + event patterns). Know how to craft test event payloads and how SAM local differs from actual Lambda execution.

### Automatizar testes de implantação

- Infrastructure as Code & Environment Management

| Sub-block | Topics |
|-----------|--------|
| IaC Templates | AWS SAM templates, CloudFormation templates, updating existing stacks, deploying to multiple environments |
| Environment Management | Dev / test / prod separation in API Gateway (stages), Lambda aliases and versions, container image tags, Amplify branches, Copilot environments, AppConfig runtime configs for dynamic deployments |

💡 SAM vs CloudFormation is a classic exam pairing — SAM is a superset of CloudFormation optimized for serverless. Lambda aliases + traffic shifting are critical for deployment strategies.

### Deploy the code using AWS Continuous Integration and Continuous Delivery (CI/CD) services

- CI/CD Pipelines & Deployment Strategies

| Sub-block | Topics |
|-----------|--------|
| CI/CD PipelineCode | Commit, CodeBuild, CodeDeploy, CodePipeline — committing code to trigger build/test/deploy actions; orchestrated workflows across environments; labels and branches for version/release management
| Deployment Strategies | Blue/green, canary, rolling/continuous deployments; application rollbacks using existing strategies; Lambda deployment packages (ZIP vs container image); API Gateway stages and custom domains; Amazon Q Developer for generating automated tests |

## 4. Troubleshooting & Optimization

### Assist in root cause analysis

| Sub-block | Topics |
|-----------|--------|
| Logs & Metrics | Querying logs in CloudWatch Logs Insights, interpreting application metrics and traces, implementing custom metrics using CloudWatch EMF (Embedded Metric Format), reviewing application health via dashboards | 
| Debugging | Debugging code to identify defects, troubleshooting deployment failures using service output logs, debugging service integration failures (Lambda ↔ API Gateway ↔ DynamoDB etc.) |

💡 CloudWatch Logs Insights query syntax appears directly in exam questions — practice writing real queries. EMF is a rising topic: know how it differs from PutMetricData.

### Instrument code for observability

### Optimize applications using AWS services and resources

---

https://docs.aws.amazon.com/pt_br/aws-certification/latest/developer-associate-02/developer-associate-02.html?refid=990e3b45-5609-4136-9ce5-fb7c47b9ec52#developer-associate-02-exam-content
