## GitOps Fundamentals - Level 1
### 📌 Learn the basics of GitOps with ArgoCD and Argo Rollouts.

#### Q1. What is GitOps?
- A marketing buzzword. It doesn't mean anything.
- It is all operations that start from Git.
- It is the same as Infrastructure as Code.
- **It is set of best-practices for deployments.**

> **Correct Answer : <br> It is set of best-practices for deployments.**

<br>

#### Q2. How are GitOps and DevOps related?
- GitOps is next thing after DevOps.
- GitOps is a subset of DevOps.
- **DevOps is a paradigm/mindset. GitOps is a set of best practices.**
- GitOps is a superset of DevOps.

> **Correct Answer : <br> DevOps is a paradigm/mindset. GitOps is a set of best practices.**

<br>

#### Q3. Is the following statement true or false? GitOps is only for Kubernetes applications.
- True
- **False**

> **Correct Answer : <br> False**

<br>

#### Q4. What is the major advantage of GitOps?
- Secure deployments.
- **Eliminating configuration drift.**
- Better artifact creation and management.
- Improved unit tests.

> **Correct Answer : <br> Eliminating configuration drift.**

<br>

#### Q5. What is a major disadvantage of GitOps?
- GitOps is not very good for auditing purposes.
- Rollbacks with GitOps are very difficult
- **GitOps handles only deployments**
- GitOps works only with containerized applications

> **Correct Answer : <br> GitOps handles only deployments**

<br>

#### Q6. What is Argo CD?
- A manager for Helm and Kustomize templates
- A certified distribution of Kubernetes
- **A Kubernetes controller**
- A solution for Kubernetes workflows

> **Correct Answer : <br> A Kubernetes controller**

<br>

#### Q7. Which other Argo products, Argo CD needs to function correctly?
- Argo CD also needs Argo Workflows and Argo Events
- Argo CD also needs Argo Rollouts
- Argo CD only needs Argo Workflows. Argo Event and Argo Rollouts are optional
- **None. Argo CD is a standalone project. It works great with the other Argo projects, but it does not depend on them.**

> **Correct Answer : <br> None. Argo CD is a standalone project. It works great with the other Argo projects, but it does not depend on them.**

<br>

#### Q8. How does Argo CD interact with clusters?
- You need to install Argo CD on every cluster that you wish to deploy
- You only need one Argo CD instance on one cluster. You can use the Argo CD CLI for other clusters
- You need one Argo CD instance for every 5 Kubernetes clusters that you wish to deploy to
- **You can have any combination of clusters and Argo CD instances. Argo CD can deploy applications on the cluster it is installed on, or other external clusters that are authenticated correctly**

> **Correct Answer : <br> You can have any combination of clusters and Argo CD instances. Argo CD can deploy applications on the cluster it is installed on, or other external clusters that are authenticated correctly**

<br>

#### Q9. How can you install Argo CD on your cluster?
- You must use a Kubernetes manifest from Git
- You must use the official Helm chart
- You must use a friendly installer such as Argo Autopilot
- **You can use any of the above including other community methods**

> **Correct Answer : <br> You can use any of the above including other community methods**

<br>

#### Q10. What is the relationship between the Argo CD Web interface and the Argo CD Command line executable?
- The Argo CD UI is only for viewing installed applications. You must use the CLI to actually deploy an application.
- The ArgoCD UI is only for managers and team leaders. Developers must use the Argo CD CLI for their needs
- **The Argo CD UI and the CLI can be used interchangeably according to your needs.**
- The Argo CD UI can only install applications on the same cluster Argo CD runs on. Only the Argo CD CLI can deploy to other clusters.

> **Correct Answer : <br> The Argo CD UI and the CLI can be used interchangeably according to your needs.**

<br>

#### Q11. Is the following statement true or false? If you have enabled the "auto-sync" option in an Argo CD application, and something is changed manually in the cluster then Argo CD will automatically discard the change.
- True
- **False**

> **Correct Answer : <br> False**

<br>

#### Q12. Is the following statement true or false? If you have enabled the "auto-sync" option in an Argo CD application, and you delete a resource in Git, then Argo CD will automatically delete that resource from the cluster as well.
- True
- **False**

> **Correct Answer : <br> False**

<br>

#### Q13. What is the proper way to handle application secrets via GitOps?
- **Encrypt them and store them in Git. Then decrypt them during runtime.**
- Put them in configmaps and use kubectl exec to pass the values directly to a pod
- Store them in the values file of a Helm chart and commit them to Git
- Put them in the Kubernetes Secret resource and make them part of a Helm chart.

> **Correct Answer : <br> Encrypt them and store them in Git. Then decrypt them during runtime.**

<br>

#### Q14. If you use Bitnami Sealed Secrets then where does encryption and decryption take place?
- Encryption happens in the Argo CD CLI. Decryption happens in the Argo CD Web interface
- Both encryption and decryption are handled by the Sealed Secrets controller.
- **Encryption happens via the kubeseal executable. Decryption happens via the Sealed Secrets controller.**
- Encryption happens by the Sealed Secrets controller. Decryption happens via the Argo CD controller

> **Correct Answer : <br> Encryption happens via the kubeseal executable. Decryption happens via the Sealed Secrets controller.**

<br>

#### Q15. You have just logged in the Argo CD UI and created an application using a Git repository that holds your Helm chart. You sync the application and everything is fine. What is the next step that you should take?
- Delete the application from the Argo CD UI and create it again using the Argo CD CLI.
- Convert the Helm chart to Kustomize files.
- **Create a declarative file of the application and other resources (e.g. Argo CD project) usedand store them in Git.**
- Go into the latest manifest inside the Argo CD Web interface and update the container image to a new version.

> **Correct Answer : <br> Create a declarative file of the application and other resources (e.g. Argo CD project) used and store them in Git.**

<br>

#### Q16. You just created a Helm application using the Argo CD web interface. You then go to the command line and enter "helm list". To your surprise nothing is printed.
- **The helm command will never work no matter what you do in Argo CD**
- You need to sync first the application using the Argo CD UI before the helm command can work
- You need to enable "auto-sync" in the Argo CD UI before the helm command can work
- You need to enable both the self-heal and the "auto-sync" option in the Argo CD UI for the helm command to work

> **Correct Answer : <br> The helm command will never work no matter what you do in Argo CD**

<br>

#### Q17. What kind of applications can Argo CD deploy?
- Argo CD can only deploy plain Kubernetes manifests
- Argo CD can only deploy Helm applications
- Argo CD can only deploy Kustomize applications
- **Argo CD can deploy all of the above**

> **Correct Answer : <br> Argo CD can deploy all of the above**

<br>

#### Q18. What is Progressive Delivery?
- **A way to gradually deploy applications minimizing downtime**
- A way to render applications even in old browsers
- A way to create an application that works on desktop computers and mobile phones
- A way to get metrics from your Kubernetes clusters

> **Correct Answer : <br> A way to gradually deploy applications minimizing downtime**

<br>

#### Q19. What is Argo Rollouts
- An extension to Argo CD for metric analysis
- **A Kubernetes controller for progressive delivery**
- An enhanced Kubernetes scheduler
- A smart installer for Argo Deployments

> **Correct Answer : <br> A Kubernetes controller for progressive delivery**

<br>

#### Q20. What is the relationship between Argo CD and Argo Rollouts
- Argo CD depends on Argo Rollouts
- Argo Rollouts depends on Argo CD
- **Argo CD and Argo Rollouts can either be deployed individually or both at the same time.**
- Argo Rollouts is an optional extension to Argo CD

> **Correct Answer : <br> Argo CD and Argo Rollouts can either be deployed individually or both at the same time.**

<br>

#### Q21. What are Blue/Green deployments?
- A deployment method where the previous version is marked as "blue" and the next version as "green"
- A deployment method for rolling Kubernetes updates
- **A deployment method where the new version is launched while the old version is stillrunning. Both version exist during the deployment**
- An advanced Kubernetes scheduling algorithm

> **Correct Answer : <br> A deployment method where the new version is launched while the old version is still running. Both version exist during the deployment**

<br>

#### Q22. What are Canary deployments
- **A deployment method where only a subset of live users get access to the new version of the application**
- A deployment method where the previous version is marked as "stable" and the next version as "canary"
- A deployment method for rolling Kubernetes updates
- An advanced Kubernetes scheduling algorithm

> **Correct Answer : <br> A deployment method where only a subset of live users get access to the new version of the application**

<br>

#### Q23. How does Argo Rollout work?
- **You need to convert your Kubernetes Deployment to a Rollout resource to enable progressive delivery**
- You need to add a Rollout configmap to your application to enable progressive Delivery
- You need to add a sealed secret first to your application to enable progressive Delivery
- You need to deploy your application with Argo CD first before enabling progressive Delivery

> **Correct Answer : <br> You need to convert your Kubernetes Deployment to a Rollout resource to enable progressive delivery**