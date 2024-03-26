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
- **Yes, they can be combined with no limitations**
- Yes, they can be combined but only if the controllers are the same version

> **Correct Answer : <br> Yes, they can be combined with no limitations**

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

#### Q18. You want to create temporary environments for developers while they create new features on different branches. The correct ApplicationSet generator to use is

- Git Generator
- List Generator
- SCM provider Generator
- **Pull Request Generator**

> **Correct Answer : <br> Pull Request Generator**

<br>

#### Q19. How can you model different GitOps environments?

- Use a branch for each environment
- Use a folder for each environment
- Use a git repository for each environment
- **Any of the above**

> **Correct Answer : <br> Any of the above**

<br>

#### Q20. How does Argo Image Updater work?

- **It monitors Docker registries for new containers**
- It monitors configmaps for new changes
- It monitors Argo CD applications for updates
- It monitors Git repositories for new commits

> **Correct Answer : <br> It monitors Docker registries for new containers**

<br>

#### Q21. You have a “staging” container tag that should always be deployed to a staging environment as soon as somebody updates it. The appropriate Argo Image updater strategy is

- name
- latest
- digest
- semver

> **Wrong Answer : <br> name**

<br>

#### Q22. You have a production environment that gets container images with tags that match only 1.x version. The appropriate Argo Image updater strategy is

- name
- latest
- digest
- **semver**

> **Correct Answer : <br> semver**

<br>

#### Q23. You have an application managed by Argo Image Updater with the “semver” strategy. The current image is tagged “1.4” with a constraint to “1.x” releases. You build a new image and push it with tag 1.2.7. This new container

- will be deployed only if it doesn’t already exist in the registry
- will be deployed only if it was deployed in the past at least once by Argo Image Updater
- will not be deployed because it doesn’t match the constraints
- **will not be deployed because 1.4 is newer**

> **Correct Answer : <br> will not be deployed because 1.4 is newer**

<br>

#### Q24. An Argo CD hook that runs in the PreSync phase has an error and fails. Argo CD will

- Continue with the resources in the Sync Phase
- Continue with the resources in the SyncFail Phase
- Continue with the resources in the Skip Phase
- **Abort the deployment**

> **Correct Answer : <br> Abort the deployment**

<br>

#### Q25. Resource A is marked with Sync wave -1 and Resource B is marked with wave 5.

- A will be deployed before B
- B will be deployed before A
- A will be placed in the PreSync phase and B in the PostSync phase
- **We need to check for sync phases before we can answer**

> **Correct Answer : <br> We need to check for sync phases before we can answer**

<br>

#### Q26. Resource A is marked with Sync Wave -1 and placed in the Presync phase. Resource B is marked with Sync Wave: -99 and placed in the Skip phase

- A will be deployed before B
- B will be deployed before A
- A and B will be deployed in parallel
- **None of the above**

> **Correct Answer : <br> None of the above**

<br>

#### Q27. Argo CD will mark an application as Failed if...

- A PreSync hook fails but PostSync hooks succeed
- A Sync hook fails but Pre and Post hooks succeed
- A FailSync hook fails but Sync hooks succeed
- **Any hook fails regardless of its phase**

> **Correct Answer : <br> Any hook fails regardless of its phase**

<br>

#### Q28. If a hook in the SyncFail phase has an error, Argo CD

- will run the SyncFail hooks again
- will run the PostSync hooks
- **will abort the deployment and mark it as failed**
- will abort the deployment and mark it as successful

> **Correct Answer : <br> will abort the deployment and mark it as failed**

<br>

#### Q29. If a hook in the PostSync phase has an error, Argo CD

- will run the SyncFail hooks
- will run the Skip hooks
- **will abort the deployment and mark it as failed**
- will abort the deployment and mark it as successful

> **Correct Answer : <br> will abort the deployment and mark it as failed**

<br>

#### Q30. Resource A is in the Sync phase and has no Sync wave. Resource B is in the Sync phase and has Sync wave 0

- A will be deployed before B
- B will be deployed before A
- A and B will be deployed in parallel
- **A and B will be deployed according to the default Resource ordering**

> **Correct Answer : <br> A and B will be deployed according to the default Resource ordering**

<br>

#### Q31. Can you use sync waves to replace sync phases?

- No, you need both sync waves and phases in an application
- Yes, anything that be done with phases can be also done with waves
- No, you need to use either sync waves or phases (but never both)
- **Yes, but only if you don’t need the SyncFail mechanism**

> **Correct Answer : <br> Yes, but only if you don’t need the SyncFail mechanism**

<br>

#### Q32. What is the relationship between Sync Waves and phases?

- Sync phases are obsolete. Use only Sync waves
- Sync waves and phases are mutually exclusive
- **Sync waves and phases can be used on their own or both at once**
- Sync phases are for Helm applications and Sync waves for Kustomize applications

> **Correct Answer : <br> Sync waves and phases can be used on their own or both at once**

<br>

#### Q33. Resource A is in the PreSync phase and Sync wave 10. Resource B is in the Sync phase and has Sync wave 20. Resource C is in the SyncFail phase with sync wave 30

- A will be deployed first, then B and then C
- A will be deployed first, then B an C will be deployed in parallel
- A will be deployed first. Then B. C will never be deployed
- C will be deployed only if B fails to deploy

> **Wrong Answer : <br>**

<br>

#### Q34. Resource A is in the PostSync phase and has Sync wave 5. Resource B is in the PostSync phase and has Sync Wave 5. Resource C is in the PostSync phase and has Sync Wave -10

- C will be deployed first and then A and B will deployed in parallel
- A and B will be deployed in parallel and then C will be deployed
- **C will be deployed first and then A and B will be deployed according to default Resource order**
- The order of deployment is undefined since all resources belong in the same Sync phase

> **Correct Answer : <br> C will be deployed first and then A and B will be deployed according to default Resource order**

<br>

#### Q35. Resource A is in the PreSync phase with Sync wave 50. Resource B is in the SyncFail phase with Sync Wave -50. Resource C is in the PostSync phase with wave -99

- Resource C will be deployed first, then Resource B, and finally Resource A
- Resource C will be deployed first then Resource A. Resource B will never be deployed
- **Resource A will be deployed first, then Resource B (if applicable). Resource C will be deployed after A (if applicable)**
- Resource A will be deployed first. Resource B will be skipped. Resource C will be deployed last

> **Correct Answer : <br> Resource A will be deployed first, then Resource B (if applicable). Resource C will be deployed after A (if applicable)**

<br>

#### Q36. Resource A is in the PreSync phase with Sync wave 50. Resource B is in the Sync phase with Sync Wave -10. Resource C is in the PostSync phase with wave 50

- Resource C will be deployed first, then Resource B, and finally Resource A
- Resource A and C will be deployed first and then Resource B
- **Resource A will be deployed first then Resource B and finally Resource C**
- Resource B will be deployed first then Resource A and C will be deployed in parallel.

> **Correct Answer : <br> Resource A will be deployed first then Resource B and finally Resource C**

<br>

#### Q37. When do you need to ignore differences in Argo CD resources?

- When you use Helm charts with subcharts
- When you store your Secrets in Configmaps
- When the application is a Kubernetes operator
- **When an application has values that should be dynamically modified after manifests are applied.**

> **Correct Answer : <br> When an application has values that should be dynamically modified after manifests are applied.**

<br>

#### Q38. What are Sync Windows used for?

- **To disable/enable application deployments for different time periods.**
- To restrict application deployment to specific Argo CD projects
- To combine Sync waves with time constraints
- To decide if users can deploy application to specific namespaces

> **Cprrect Answer : <br> To disable/enable application deployments for different time periods.**

<br>

#### Q39. An application has an “allow” sync window for 5pm to 6pm. The time is now 7pm

- You can deploy the application as no sync window is active
- You can deploy the application because no “deny” window is active
- **You cannot deploy the application because no “allow” window is active**
- You cannot deploy the application because a “deny” window is active

> **Correct Answer : <br> You cannot deploy the application because no “allow” window is active**

<br>

#### Q40. An application has a “deny” sync window for 5pm to 6pm. The time is now 7pm

- You can deploy the application because an “allow” window is active
- **You can deploy the application because no “deny” window is active**
- You cannot deploy the application because no “allow” window is active
- You cannot deploy the application because a “deny” window is active

> **Correct Answer : <br> You can deploy the application because no “deny” window is active**

<br>

#### Q41. An application has a “deny” sync window for 5pm to 8pm and an “allow” sync window from 6pm to 9pm. The time is now 7pm

- You can deploy the application because an “allow” window is active
- You can deploy the application because no “deny” window is active
- **You cannot deploy the application, “deny” windows override “allow” windows**
- You cannot deploy the application because of the situation as overlapping sync windows are not allowed.

> **Correct Answer : <br> You cannot deploy the application, “deny” windows override “allow” windows**

<br>

#### Q42. An application has a “deny” sync window for 5pm to 7 pm, an “allow” sync window from 4pm to 8pm. The time is now 6pm

- You can deploy the application because an “allow” window is active
- You can deploy the application because the “allow” window has a larger period than the “deny” window
- **You cannot deploy the application, “deny” windows override “allow” windows**
- You cannot deploy the application because of the situation as overlapping sync windows are not allowed

> **Correct Answer : <br> You cannot deploy the application, “deny” windows override “allow” windows**

<br>

#### Q43. An application has a “deny” sync window for 5pm to 7 pm, an “allow” sync window from 4pm to 7pm and an “allow” window from 5:30 to 6:30pm. The time is now 6pm

- You can deploy the application because two “allow” windows are active
- You can deploy the application because there are more “allow” windows than “deny” windows
- You cannot deploy the application, “deny” windows override “allow” windows
- **You cannot deploy the application because of the situation as overlapping sync windows are not allowed**

> **Wrong Answer : <br> You cannot deploy the application because of the situation as overlapping sync windows are not allowed**

<br>

#### Q44. What is the best way according to the GitOps principles to update the container of an application

- Use “kubectl edit” to change the manifest in the cluster
- Use the Argo CD UI to “edit” the manifest of the application
- **Use your CI system to commit a change in the manifest stored in the git repository**
- Use Argo Image updater and the “Argo CD write back” method

> **Correct Answer : <br> Use your CI system to commit a change in the manifest stored in the git repository**

<br>

#### Q45. What is the major disadvantage of disabling “self-heal” in an application

- The application can no longer be redeployed by git changes
- **Manual changes in the cluster will no longer be detected and discarded**
- The CI system can no longer monitor application deployment
- The Argo CD UI will show the application as “out-of-sync” after each deployment

> **Correct Answer : <br> Manual changes in the cluster will no longer be detected and discarded**

<br>

#### Q46. What is the major advantage of using folders as GitOps environments?

- You can promote any change from any environment to any other environment
- The order of commits is no longer relevant for environment promotions
- Handling a large number of environments always results in managing a single git branch
- **All the above**

> **Correct Answer : <br> All the above**

<br>

#### Q47. What is the major disadvantage of using folders as GitOps environments?

- Developer don’t know how to use the “cp “command
- The number of folders is twice the number of environments
- Argo CD has limitations with handling subfolders in a git repository
- **It is difficult to secure individual folders in a single git repository**

> **Correct Answer : <br> It is difficult to secure individual folders in a single git repository**

<br>

#### Q48. What is the major advantage of using branches as GitOps environments?

- **Developers are already familiar with how git tools work**
- A large number of environments can be easily modeled with only a few branches
- Helm and Kustomize have native support for using git branches as different overlays/values
- Configuration drift is avoided by avoiding the usage of “git cherry-pick”

> **Correct Answer : <br> Developers are already familiar with how git tools work**

<br>

#### Q49. What is the major disadvantage of using branches as GitOps environments?

- **Order of commits affects every promotion done by merging**
- Argo CD does not support picking individual branches for an application
- Developers familiar with Git-flow cannot use Argo CD for manifest repositories
- Manual approvals for deployments are no longer possible

> **Correct Answer : <br> Order of commits affects every promotion done by merging**

<br>

#### Q50. What is the best way of modeling your GitOps environments?

- Using git Branches for environments
- Using folders in a single git repository
- Using multiple git repositories (one for each environment)
- **It depends according to the assumptions and limitations of your organization**

> **Correct Answer : <br> It depends according to the assumptions and limitations of your organization**
