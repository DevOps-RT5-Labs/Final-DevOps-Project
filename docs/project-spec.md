# Project Specifications

This document describes the specifications of the DevOps project, including the requirements, and the tools of the implementation.

## Requirements

- The Project is a web application architected as a microservice and managed in Agile.
  - The Project should be implemented using the [Microservice Architecture](https://microservices.io/patterns/microservices.html) and Hexagonal Architecture.
  - The Project should be managed using a suitable Agile/Kanban tool.
  - The Web Application should have a Documented API for the Backend.
  - The Web Application should have a Documented Code for the Internal Code.
  - The Web Application should have a Documented API for the UI.
  - The Web Project should publish Traceable Logs.
  - The Web Project should publish Traceable Spans.
- The Project Development Environment should be easy to manage and use.
  - All the code should be in a single git repository (Monorepo pattern).
  - Commit messages should follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.
  - Branch names should follow the [GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) specification.
  - All Merges to the `develop` branch should be done using Pull Requests and should be reviewed by at least one other developer.
  - Commands and Scripts should be abstracted and centralized in a Makefile.
  - Validating the Tools and Setting up the Environment should be easy and automated.
  - Multiple Environments should be available (Development, Testing, Staging, Production).
- The Project Configurations should be easy to manage and configure.
  - Environment Variables should be used for all the configurations and should be centralized
  - The Project deployment should be easily configurable and manageable.
  - The Project infrastructure should be easily configurable and manageable.
- The Project should have a complete Continuous Integration (CI) pipeline for every component.
  - All the components should have a Dockerfile.
  - All the components should have a CI pipeline, where they are built, tested, and published to a registry.
- The Project should be testable, and QA should be highly considered and implemented.
  - The Project should have Unit Tests, Integration Tests, and End-to-End Tests.
  - The Tests should generate a report that can be used to monitor the project health.
  - A QA monitoring tool should be used to monitor the project health.
  - The Project should have a Test Deployment pipeline.
  - The Project should have performance tests.
- The Project should be easy to deploy and manage.
  - The Project should be deployed to a Kubernetes Cluster.
  - The Project should have a Deployment pipeline.
  - The Project should follow GitOps for the deployment.
  - Deployment strategies should be implemented.
- The Project should be easy to monitor and debug.
  - A Dashboard should be implemented to monitor all the traceable details.
  - Metrics should be traceable.
  - Logs should be traceable.
  - Spans should be traceable.
  - Alerts should be implemented.
  - FinOps can be considered.
- The Project should follow Security best practices.
  - All Secrets should be encrypted and easily managed
  - Code Security and Quality should be managed and monitored.
  - Deployment Security Configuration should be monitored.
  - Optional: Backups should be implemented.
  - Optional: Open Policy Agent can be considered.
  - Optional: Supply Chain Security can be considered.
- The Project should be highly documented.
    - The Project should have an End-User Documentation.
    - The Project should have a Deployment Documentation.
    - The Project should have a CI/CD Documentation.
    - The Project should explain how best practices are implemented.

## Management / Technical Choices
- Kanban Board: [GitHub Projects](https://github.com/orgs/DevOps-RT5-Labs/projects/1/views/1)
- Code Related Choices
  - Implementation: Typescript, ReactJS, GoLang
  - Logging: Zap
  - Span Tracing: Jaeger
  - Internal Code Documentation: GoDoc
  - API Documentation: Swagger
  - UI Documentation: Storybook
- Environment
  - Multiple Environments: Kubernetes Namespaces
  - Commands: Makefile
- Configuration
  - Environment Variables: ConfigMaps, Secrets
  - Deployment: Kustomize
  - Infrastructure: Terraform
- Testing
  - Unit Testing: Go Testing
  - Integration Testing: Go Testing
  - End-to-End Testing: Cypress
  - Performance Testing: k6
  - QA Monitoring: SonarQube
- CI/CD
  - Pipeline: TBD
  - Docker Registry: DockerHub
- Deployment
  - Platform: Kubernetes
  - GitOps: ArgoCD
  - Deployment Strategies: Blue/Green, Canary..
- Monitoring
  - Dashboard: Grafana
  - Metrics: Prometheus
  - Logs: Loki
  - Spans: Jaeger
  - Alerts: Prometheus AlertManager
  - FinOps: KubeCost
- Security
  - Secrets Management: HashiCorp Vault, External-Secrets
  - Backups: Velero
  - Open Policy Agent: Gatekeeper
  - Supply Chain Security: Depends on the CI/CD Pipeline
  - Configuration Security: Datree
- Documentation: Markdown


## Open Questions
- What are some best practices that we should follow (GitOps, DevOps, Git..)?
- Frontend Level Logging (Sentry?)
- Test Deployment leads to staging URL