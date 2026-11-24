# CloudPulse — AWS Event Processing Platform

## One-line pitch
A cloud-native service that accepts events over an API, queues work reliably, processes it asynchronously, and exposes delivery status and operational health.

## Why this project
Shows backend design, AWS fundamentals, asynchronous processing, infrastructure as code, observability, and deployment discipline.

## MVP
- API accepts an event with an idempotency key.
- Persist event metadata and enqueue work.
- Worker processes events with retry and dead-letter handling.
- Status endpoint reports accepted, processing, completed, and failed states.
- Dashboard or README screenshots show logs, metrics, and alarms.

## Suggested AWS architecture
API Gateway + Lambda, SQS with a dead-letter queue, Lambda worker, DynamoDB, CloudWatch, and Terraform. Keep the first version serverless to make the architecture affordable and easy to reproduce.

## Quality bar
- Idempotent submissions and bounded retries.
- Least-privilege IAM policies and secrets management.
- Terraform plan/apply instructions and a clean teardown path.
- Structured logs, useful metrics, and alarms for errors and queue age.
- Cost estimate and documented design tradeoffs.

## Build sequence
1. Write the event contract and state transitions.
2. Implement a local version with tests and a queue abstraction.
3. Provision AWS resources with Terraform.
4. Add retries, DLQ, alarms, and deployment automation.
5. Capture architecture, cost assumptions, and a failure/recovery demo.

## Resume bullet template
Designed and deployed an event processing platform on AWS using [services], handling [measured throughput] with [measured reliability], retries, dead-letter recovery, and infrastructure as code.

## Status
Planned. Add measured throughput, cost, and reliability only after running load and failure tests.
