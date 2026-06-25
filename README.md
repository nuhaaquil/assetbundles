# Databricks Asset Bundles Project

## Overview

This project demonstrates the implementation of Databricks Asset Bundles (DAB) for managing and deploying Databricks resources using Infrastructure as Code (IaC).

The project includes:

* Lakeflow Jobs
* Lakeflow Declarative Pipelines (Delta Live Tables)
* Environment-specific configurations
* Dynamic variable management
* Development and Production deployments
* Bundle validation and deployment using Databricks CLI

---

## Project Structure

```text
dabproject/
│
├── databricks.yml
├── resources/
│   ├── Jobs/
│   │   └── job.yml
│   ├── pipelines/
│   │   └── demopipeline.yml
│   └── variables/
│       └── variables.yml
│
├── src/
│   ├── notebooks/
│   │   └── ingestion.ipynb
│   └── pipelines/
│       └── demopipeline/
│           └── transformations/
│
└── README.md
```

---

## Technologies Used

* Databricks Asset Bundles
* Databricks CLI
* Lakeflow Jobs
* Lakeflow Declarative Pipelines (DLT)
* Unity Catalog
* YAML Configuration
* Git & GitHub

---

## Features

### Asset Bundle Configuration

* Centralized bundle definition using `databricks.yml`
* Environment-specific deployment targets
* Reusable resource definitions
* Infrastructure as Code approach

### Lakeflow Job

* Notebook-based ingestion workflow
* Parameterized execution using bundle variables

### Declarative Pipeline

* Serverless pipeline execution
* Unity Catalog integration
* Dynamic catalog configuration

### Environment Management

* Development Environment
* Production Environment
* Variable-based configuration management

---

## Variables

The project uses bundle variables to dynamically configure deployments.

Example:

```yaml
variables:
  catalog_name:
    default: assetbundles
```

During deployment:

```bash
databricks bundle deploy --target prod --var="catalog_name=assetbundles_prod"
```

---

## Validation

Validate bundle configuration before deployment:

```bash
databricks bundle validate --target dev
```

---

## Deployment

### Development

```bash
databricks bundle deploy --target dev
```

### Production

```bash
databricks bundle deploy --target prod --var="catalog_name=assetbundles_prod"
```

---

## Learning Outcomes

Through this project, I learned:

* Databricks Asset Bundles fundamentals
* Bundle configuration and structure
* Resource management using YAML
* Lakeflow Jobs creation and deployment
* Lakeflow Declarative Pipelines (DLT)
* Environment-specific deployments
* Variable-driven configuration
* Databricks CLI operations
* Git integration and version control
* Infrastructure as Code concepts in Databricks

