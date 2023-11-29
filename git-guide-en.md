**[EN-US]**
## **What is Git and GitHub for?**

**Git** is a version control system, which means it manages changes in software projects over time. It allows multiple people to work on a project simultaneously, tracks changes made, and facilitates collaboration.

**GitHub**, on the other hand, is a code hosting platform that uses Git. It's like a social network for developers, where they can store, share, and collaborate on projects using Git. GitHub provides a user-friendly web interface for working with Git repositories, making it easier for development teams to collaborate on software projects.

In summary, Git is the underlying technology that manages project versions, and GitHub is a platform that uses Git to facilitate collaboration and source code management.

---

## ******************************How to download and install Git.******************************

1. **Download Git:**
    - Go to the official Git website at [git-scm.com](https://git-scm.com/).
    - Click on the download button for your operating system (Windows, macOS, Linux, etc.).
2. **Install Git:**
    - On Windows, run the downloaded installer and follow the standard instructions.
    - On macOS, you can use Homebrew or the graphical installer.
    - On Linux, use your distribution's package manager.
    
    ---

## **Configuring Git.**

1. **Open the Terminal:**
    - This is where you will interact with Git.
2. **Set your username:**
    
    ```bash
    git config --global user.name "Your Name"
    ```
    
3. **Set your email address:**
    
    ```bash
    git config --global user.email "your.email@example.com"
    ```
    

### **Check Settings:**

To check if the settings were configured correctly, type:

```bash
git config --global --list
```

This should display your global configurations.

---

## **Local and Remote Repository.**

### **Local Repository:**

- It is the version of your project stored on your computer. You interact directly with this repository, making changes, commits, etc.

### **Remote Repository:**

- It is the version of your project hosted on a remote server, such as GitHub. It is used for collaboration and sharing. You send your changes from the local repository to the remote one.

---

## Git and GitHub Commands.

### Git Commands:

**`git init`**: This command is used to start a new Git repository. When you create a new project, you can run **`git init`** in the project directory to begin tracking changes.

---

**`git clone`**: Used to clone (copy) an existing repository. You provide the repository URL **`git clone url`**, and Git creates a complete local copy on your computer.

---

**`git add`**: Adds changes to the next commit. It can be a specific file (**`git add filename`**) or all changes in the directory (**`git add .`**).

---

**`git commit`**: Commits the changes that were added with **`git add`**. Each commit has a message describing the changes made, like `git commit -m`.

---

**`git diff`**: Shows the differences between your current working directory and the last commit.

---

**`git rm`**: Removes files from version control. It also physically removes the files from your working directory.

---

**`git status`**: Shows the current state of your repository. Indicates which files have been modified, added, or are pending for commit.

---

**`git log`**: Displays the commit history, showing who made what changes and when.

---

**`git restore`**: Undoes changes in the working directory. Can be used to undo specific changes or even restore a deleted file.

---

**`git branch`**: Lists the existing branches in your repository.

---

**`git branch new-branch`**   : Creates a new branch in the current repository.

---

**`git checkout`**  or  **`git switch`**: Switches to a specific branch. Can also be used to create a new branch **`git checkout -b new-branch`**  or  **`git switch -c new-branch`.**

---

**`git merge`**: Combines the changes from one branch into another. For example, to merge the work from a feature branch back into the main branch.

---

**`git fetch`**: Fetches changes from the remote repository but does not merge them into your working directory.

---

**`git pull`**: Fetches changes from the remote repository and automatically merges them into your working directory.

---

**`git push`**: Sends local changes to the remote repository. Useful when you want to share your work or backup changes online.

---

### GitHub Commands:

**`git remote add origin <URL>`**: Connects the local repository to a remote repository on GitHub.

---

**`git push -u origin <branch>`**: Sets the default remote branch.

---

**Pull Request (PR)**: Used to propose changes and initiate a discussion before merging them.

---

**Issues**: Tracks tasks, improvements, or bugs.

---

**Fork**: Creates an independent copy of a repository so that you can contribute without affecting the original.

---

**Clone or download**: Provides the URL that you can use with **`git clone`**.

---

**Settings**: Repository settings, where you can manage collaborators, access, and other configurations.

---

# Commit Patterns.

According to the **[Conventional Commits](https://www.conventionalcommits.org/)** documentation, semantic commits are a simple convention to be used in commit messages. This convention defines a set of rules to create an explicit commit history, making it easy to create automated tools.

These commits will help you and your team easily understand what changes were made in the committed code.

This identification is done through a word and an emoji that identifies if that commit is related to code changes, package updates, documentation, visual changes, tests...

---

## Type and Description:

The semantic commit has the following structural elements (types), which inform the intention of your commit to the code user.

- `feat`- Commits of type feat indicate that your piece of code is including a **new feature** (related to MINOR in semantic versioning).

- `fix` - Commits of type fix indicate that your committed piece of code is **fixing a problem** (bug fix), (related to PATCH in semantic versioning).

- `docs` - Commits of type docs indicate that there have been **changes in documentation**, such as in your repository's Readme. (Does not include code changes).

- `test` - Commits of type test are used when **changes are made to tests**, whether creating, modifying, or deleting unit tests. (Does not include code changes)

- `build` - Commits of type build are used when modifications are made to **build and dependency files**.

- `perf` - Commits of type perf are used to identify any code changes related to **performance**.

- `style` - Commits of type style indicate that there have been changes related to **code formatting**, semicolons, trailing spaces, lint... (Does not include code changes).

- `refactor` - Commits of type refactor refer to changes due to **refactorings that do not change functionality**, such as a change in the format of a certain part of the screen, but that maintained the same functionality, or performance improvements due.
  
- `chore` - Commits of type chore indicate **task updates** for build, admin settings, packages... for example, adding a package to gitignore. (Does not include code changes)

- `ci` - Commits of type ci indicate changes related to **continuous integration**.

- `raw` - Commits of type raw indicate changes related to configuration files, data, features, parameters.

## Recommendations:

- Add a type consistent with the content title.
- We recommend that the first line should have a maximum of 4 words.
- For detailed descriptions, use the commit description.
- Use an emoji at the beginning of the commit message representing the commit.

## Commit Add-ons:

- **Footer:** information about the reviewer and card number on Trello or Jira. Example: Reviewed-by: Elisandro Mello Refs #133
- **Body:** more precise descriptions of what is contained in the commit, presenting impacts and the reasons for the code changes, as well as essential instructions for future interventions. Example: see the issue for details on typos fixed.
- **Descriptions:** a succinct description of the change. Example: correct minor typos in code

## Emoji Patterns:

| Commit Type           | Emoji               | Keyword        |
|-----------------------|---------------------|----------------|
| Accessibility        | ♿ `:wheelchair:`    |                |
| Adding a test         | ✅ `:white_check_mark:` | `test`       |
| Adding a dependency   | ➕ `:heavy_plus_sign:` | `build`       |
| Code review changes   | 👌 `:ok_hand:`       | `style`        |
| Animations and transitions | 💫 `:dizzy:`    |                |
| Bugfix                | 🐛 `:bug:`           | `fix`          |
| Comments              | 💡 `:bulb:`          | `docs`         |
| Initial commit        | 🎉 `:tada:`          | `init`         |
| Configuration         | 🔧 `:wrench:`        | `chore`        |
| Deploy                | 🚀 `:rocket:`        |                |
| Documentation         | 📚 `:books:`         | `docs`         |
| In progress           | 🚧 `:construction:`  |                |
| Interface styling     | 💄 `:lipstick:`      | `feat`         |
| Infrastructure        | 🧱 `:bricks:`        | `ci`           |
| Ideas/tasks list      | 🔜 `:soon:`          |                |
| Move/Rename           | 🚚 `:truck:`         | `chore`        |
| New feature           | ✨ `:sparkles:`      | `feat`         |
| Package.json in JS    | 📦 `:package:`       | `build`        |
| Performance           | ⚡ `:zap:`           | `perf`         |
| Refactoring           | ♻️ `:recycle:`       | `refactor`     |
| Remove a file         | 🔥 `:fire:`          |                |
| Remove a dependency   | ➖ `:heavy_minus_sign:` | `build`      |
| Responsiveness        | 📱 `:iphone:`        |                |
| Revert changes        | 💥 `:boom:`          | `fix`          |
| Security             | 🔒️ `:lock:`          |                |
| SEO                   | 🔍️ `:mag:`           |                |
| Version tag          | 🔖 `:bookmark:`       |                |
| Approval test        | ✔️ `:heavy_check_mark:` | `test`        |
| Tests                | 🧪 `:test_tube:`       | `test`         |
| Text                 | 📝 `:pencil:`          |                |
| Typing               | 🏷️ `:label:`           |                |
| Error handling       | 🥅 `:goal_net:`        |                |
| Data                 | 🗃️ `:card_file_box:`  | `raw`          |

## Examples:

| Git Command                                  | GitHub Result                      |
|----------------------------------------------|------------------------------------|
| `git commit -m ":tada: Initial commit"`      | 🎉 Initial commit                 |
| `git commit -m ":books: docs: Update README"`| 📚 docs: Update README            |
| `git commit -m ":bug: fix: Infinite loop on line 50"` | 🐛 fix: Infinite loop on line 50 |
| `git commit -m ":sparkles: feat: Login page"` | ✨ feat: Login page                |
| `git commit -m ":bricks: ci: Modify Dockerfile"` | 🧱 ci: Modify Dockerfile         |
| `git commit -m ":recycle: refactor: Convert to arrow functions"` | ♻️ refactor: Convert to arrow functions |
| `git commit -m ":zap: perf: Improve response time"` | ⚡ perf: Improve response time |
| `git commit -m ":boom: fix: Revert inefficient changes"` | 💥 fix: Revert inefficient changes |
| `git commit -m ":lipstick: feat: Styling CSS for form"` | 💄 feat: Styling CSS for form     |
| `git commit -m ":test_tube: test: Create new test"` | 🧪 test: Create new test          |
| `git commit -m ":bulb: docs: Comments on LoremIpsum( ) function"` | 💡 docs: Comments on LoremIpsum( ) function |
| `git commit -m ":bulb: raw: RAW Data for year aaaa"` | 🗃️ raw: RAW Data for year aaaa   |
```
