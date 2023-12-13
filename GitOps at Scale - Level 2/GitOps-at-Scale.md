## GitOps at Scale - Level 2
### 📌 Learn sound strategies for managing applications and version deployments across multiple environments.

#### Q1. What is the Apps of Apps pattern?
- **A way to group multiple Argo CD applications together**
- A way to convert multiple git repositories in a monorepo
- A pattern for defining application startup order
- A way to connect your CI platform and Argo CD together

> **Correct Answer : <br> A way to group multiple Argo CD applications together**

<br>

#### Q2. How does the Apps of Apps pattern work?
- **You create an Argo CD application that points to other applications**
- You deploy an Argo CD application in the argocd namespace
- You combine all your applications in a single Helm chart
- You use the ApplicationSets controller to autogenerate applications

> **Correct Answer : <br> You create an Argo CD application that points to other applications**

<br>