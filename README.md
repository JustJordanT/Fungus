# Project Fungus: GitOps for Terraform Infrastructure Deployment

![image](https://github.com/JustJordanT/Fungus/assets/38886930/065f2f78-1e7c-474a-9888-6607dade2198)


## Project Summary:
Project Fungus aims to create a GitOps tool similar to ArgoCD but specifically designed for Terraform infrastructure deployments. The tool will continuously monitor designated repositories for changes in the Terraform code, and upon detecting changes, it will automatically apply those changes to deploy and manage the corresponding infrastructure. This streamlined approach will enhance collaboration, version control, and automated deployment within infrastructure management using GitOps principles.


```mermaid
graph TD
    subgraph "Terraform Code Repositories"
        A((Repo 1)) --> |Terraform Code| B{{Fungus}}
        C((Repo 2)) --> |Terraform Code| B
        D((Repo 3)) --> |Terraform Code| B
    end

    subgraph "Fungus - GitOps Tool"
        B --> |Monitor Changes| E[Detect Changes]
        E --> |Changes Detected| F[Retrieve Terraform Code]
        F --> |Apply Changes| G[Deploy Infrastructure]
    end

    subgraph "Infrastructure"
        G --> |Automated Deployment| H[Infrastructure Components]
    end

    subgraph "Users and Collaboration"
        I[Developers/Operators] --> B
        I --> C
        I --> D
        I --> H
    end
```
