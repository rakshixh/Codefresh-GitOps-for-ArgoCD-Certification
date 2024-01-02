<h1>✨ Contributing Guide</h1>

First of all, thank you for taking the time to contribute! 🎉<br>
The following is a set of guidelines for contributing to this repository.<br>
Before contributing, we encourage you to read our [Code of Conduct](https://github.com/rakshixh/Codefresh-GitOps-for-ArgoCD-Certification/blob/main/.github/CODE_OF_CONDUCT.md).

<h2>📝 Contributing to the repository</h2>

- Cloning the Repository (repo)
- Making your Changes
- Opening a Pull Request

### Cloning the Repository

#### 1. Fork the Repository
Click the fork button at the top right of the page to create a copy of this repo in your account, or go to this repository's [fork page](https://github.com/rakshixh/Codefresh-GitOps-for-ArgoCD-Certification/fork). After successfully forking the repo, you will be directed to your repo copy.

#### 2. Clone the Forked Repository
On your forked repo, click the green button that says `Code`. It will open a dropdown menu. Copy the link in the input with the label `HTTPS` or `GitHub CLI` depending on your preferred cloning mode.

For `HTTPS`, open up your terminal and run the following command:
```bash
git clone <your-clone-link>
# or
git clone https://github.com/<your-username>/Codefresh-GitOps-for-ArgoCD-Certification.git
```
Replace `<your-username>` with your GitHub username.<br>

You can also clone the repo using the `GitHub CLI`. To do this, run the following command:
```bash
gh repo clone <your-username>/Codefresh-GitOps-for-ArgoCD-Certification
```

### Making your Changes

#### 1. Create a New Branch
Create a new branch from the main branch. Your branch name should be descriptive of the changes you are making along with your first name. Some ideas to get you started:

- For documentation: `docs-<your-first-name>`
- For adding new questions: `new-q-<your-first-name>`

To create a new branch, use the following command:
```bash
git checkout -b <your-branch-name>
```

#### 2. Make your Changes
To add new questions, follow the given format of markdown.

```
#### Q<Question Number Goes here>. <Your Question Goes here>
- **<Option A (Correct)>**
- <Option B>
- <Option C>
- <Option D>

> **Correct Answer : <br> <Option A (Correct)>**

<br>
```

>[!NOTE]
>You can add the `Correct Option` in any place but make sure to add `**` at the beginning and the end of the option.

Eg:
```
#### Q14. Garampani Sanctuary is located at?
- Junagarh, Gujarat
- **Diphu, Assam**
- Kohima, Nagaland
- Gangtok, Sikkim

> **Correct Answer : <br> Diphu, Assam**

<br>
```

> [!IMPORTANT]
> You are to make only `one contribution` per `pull request`. It makes it easier to review and merge. If you want to add `multiple new questions` or if you have solved `multiple issues`, create `separate pull requests` for each.

#### 3. Commit your Changes
Your commit message should give a concise idea of the issue you are solving. Please be specific about the commit message.

To commit your changes, run the following command:
```bash
git add .
git commit -m "<your_commit_message>"
```

Eg:
```bash
git commit -m "adding new questions to GitOps Fundamentals Level 1"
```
Push your local commits to your remote repository.
```bash
git push origin <your-branch-name>
```

### Opening a Pull Request(PR)

#### 1. Create a new Pull Request(PR)
Go to the [Codefresh-GitOps-for-ArgoCD-Certification](https://github.com/rakshixh/Codefresh-GitOps-for-ArgoCD-Certification) repository and click the `compare & pull request` button or go to the [Pull Request](https://github.com/rakshixh/Codefresh-GitOps-for-ArgoCD-Certification/pulls) page and click on the `New pull request` button. It will take you to the `Open a pull request` page.

> Note: Make sure your PR points to the `main` branch, not any other one.

#### 2. Wait for the Review
🎉 Congratulations! You've made your pull request! A maintainer will review and merge your code or request changes. If changes are requested, make them and push them to your branch. Your pull request will automatically track the changes on your branch and update.
