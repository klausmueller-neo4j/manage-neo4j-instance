# Manage Neo4j Aura Instances

Automate the **start** and **stop** of Neo4j Aura instances containing a specific keyword in their names using GitHub Actions.

## Features

- **Automated Scheduling**: 
  - **Start Instances**: Every weekday at **9 AM UTC-3**.
  - **Stop Instances**: Every weekday at **6 PM UTC-3**.
- **Manual Triggers**: Run workflows on-demand via GitHub Actions.
- **Secure Credentials**: Utilizes GitHub Secrets to manage API credentials.

## Prerequisites

- **GitHub Repository**: Where the workflows and scripts will reside.
- **Neo4j Aura Account**: With API access and necessary credentials.

## Setup

### 1. Add Repository Secrets

To securely provide your API credentials to the workflows, add the following secrets to your GitHub repository:

- `CLIENT_ID`: Your Neo4j Aura API client ID.
- `CLIENT_PWD`: Your Neo4j Aura API client password.
- `TENANT_ID`: Your Neo4j Aura tenant ID.
- `INSTANCE_NAMES_COMMA`: Comma-separated list of Neo4j Aura instance names.

#### How to Add Secrets:

1. Navigate to your repository on GitHub.
2. Click on **Settings**.
3. In the left sidebar, select **Secrets and variables** > **Actions**.
4. Click **New repository secret** and add each secret (`CLIENT_ID`, `CLIENT_PWD`, `TENANT_ID`,`INSTANCE_NAMES_COMMA`).

_For detailed instructions on creating API credentials, refer to [Neo4j Aura API Authentication](https://neo4j.com/docs/aura/platform/api/authentication/#_creating_credentials)._

### 2. Workflow Files

Place the following workflow YAML files in the `.github/workflows/` directory of your repository.
