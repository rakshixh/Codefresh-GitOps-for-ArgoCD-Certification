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

#### Q3. Where should you deploy an Argo CD application manifest?
- In the “argo” namespace
- **In any namespace defined by the Argo CD admin.**
- In the "default" or “kube-system” namespace
- In any namespace of a cluster that has Argo CD installed (apart from kube-system)

> **Correct Answer : <br> In any namespace defined by the Argo CD admin.**

<br>

#### Q4. If you define “self-heal” for a root application that contains other applications...
- **Self-heal is enabled only for the parent app**
- Self-heal is enabled only for the children apps
- Self-heal is enabled for both parent and child apps
- Self-heal is enabled only for the parent app if children apps have it enabled as well

> **Correct Answer : <br> Self-heal is enabled only for the parent app**

<br>

#### Q5. How can you use the Apps of Apps pattern?
- For grouping multiple apps together
- For cluster bootstrapping
- For automated application creation via git monitoring
- **All of the above**

> **Correct Answer : <br> All of the above**

<br>

#### Q6. How does Argo CD manage Kubernetes clusters?
- You need to install an Argo CD instance on every deployment cluster
- You need a central Argo CD instance that manages all your clusters
- You need multiple Argo CD instances that manage subsets of your clusters
- **All of the above are valid scenarios**

> **Correct Answer : <br> All of the above are valid scenarios**

<br>

#### Q7. When you add an external cluster in Argo CD…
- **You need a context for the target cluster and the CLI authenticated to the management cluster**
- You need a Kubernetes context for both clusters
- You need the Argo CD CLI authenticated to both clusters
- You need Argo CD API access to both clusters

> **Correct Answer : <br> You need a context for the target cluster and the CLI authenticated to the management cluster**

<br>

#### Q8. When you add an external/target cluster in Argo CD...
- **The management cluster needs network access to the target cluster**
- The target cluster needs outgoing network access to the management cluster
- The target cluster needs to be installed in a VPC first
- Both clusters must be part of the same VPC

> **Correct Answer : <br> The management cluster needs network access to the target cluster**

<br>

#### Q9. It's possible to add an external cluster to Argo CD…
- Using the CLI
- Using the UI only
- Using either the UI or the CLI
- Using the UI for adding the cluster and the CLI for inspecting the cluster

> **Wrong Answer : <br> Using the UI only**

<br>

#### Q10. What is the relationship between Application Sets and Apps of Apps?
- App of Apps is the next version of Application Sets
- Application Sets are the next version of Apps of Apps
- Application Sets is the rewrite of Apps of Apps
- **Both approaches are independent of each other**

> **Correct Answer : <br> Both approaches are independent of each other**

<br>

#### Q11. Can you use Application Sets with App of Apps applications?
- No, the respective controllers are not compatible with each other
- No, because they use different installation namespaces
- **Yes,  they can be combined with no limitations**
- Yes, they can be combined but only if the controllers are the same version

> **Correct Answer : <br> Yes,  they can be combined with no limitations**

<br>

#### Q12. For what scenarios can you use Application Sets?
- For installing multiple instances of an application to multiple clusters
- For installing multiple applications on a single cluster
- For installing multiple applications to multiple clusters
- **All of the above**

> **Correct Answer : <br> All of the above**

<br>

#### Q13. How do Application Sets work?
- **Application Sets are generators for Argo CD applications**
- Application Sets are used for managing Helm subcharts
- Application Sets combine Helm and Kustomize in a single Application
- Application Sets are used to split Applications from their manifests

> **Correct Answer : <br> Application Sets are generators for Argo CD applications**

<br>

#### Q14. What source can be used for Application Sets?
- A hardcoded list of applications
- A dynamic list of applications stored in git folders
- A dynamic list of applications defined in Github Pull Requests
- **All of the above**

> **Correct Answer : <br> All of the above**

<br>

#### Q15. How can you combine Application Set Generators?
- **By using a matrix generator**
- By using a list generator
- By using a git generator with different folders
- By using a git generator with different branches

> **Correct Answer : <br> By using a matrix generator**

<br>

#### Q16. You want an Argo CD application to be deployed as soon as somebody creates a new Github repository with manifests. Which ApplicationSet generator should be used?
- **SCM provider Generator**
- Pull Request Generator
- List Generator
- Git Generator

> **Correct Answer : <br> SCM provider Generator**

<br>

#### Q17. You have lots of applications in a single Git repository under “/infra/apps/”. The correct ApplicationSet generator to use is
- **Git Generator**
- List Generator
- SCM provider Generator
- Pull Request Generator

> **Correct Answer : <br> Git Generator**

<br>