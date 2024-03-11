---
title: "Github Foundation"
date: "2024-03-08" 
tags:
  - "github"
  - "git"
  - "certification"
  - "commit"
  - "teaching"
  - "copilot"
  - "codespace"
  - "standards"
---

Recently, GitHub has introduced certifications to demonstrate expertise in GitHub technologies and workflows. Acquiring a GitHub Certification may provide a competitive advantage in the job market. 


This post summarizes few basic of Github Foundation  

# What is Github?

Github is VERSION CONTROL SERVICE that initially offered to hosting managed remote git repositories ad has expanded their service offerings around the hosted codebase 

- Git Repository Hosting
- Project Management Tools (projects and projects classic)
- Issue tracking
- Pull requests and Code review
- Github Pages (for hosting static sites) 
- Github Actions
- Github Copilot 
- Github Codespaces
- Github Marketplace
- Github Gists
- Github Discussions
- Colloboration Features (Orgs and Teams)
- API access and Dev tools (Github Desktop and CLI)
- Security Features - (code scanning, secret scanning etc)
- Educatonal resources and course automation 

⭐️ *Fun fact - Github is originally built using Ruby on Rails*

1. Understand the difference Github plans and features is important. There are 3 types of Github accounts - **Personal, Organizational and Enterprise**
   Github Organization has three plans : **Free Teams and Enterprise**

    **Github Free**
      - 500 MB github package storage
      - 120 Codespace hours/month
      - 15 GB codespace storage /month
      - 2000 minutes/month of Github Actions
      - Deployment protection rules for public repo
      - Dependentbot alert
      - 2FA (for all accounts, which is good ) 
      - Only community support (which is very good!)
    
    **Github Pro**
      - Everything from Github Free account and....
      - Support via email 
      - 3000 minutes/month of Github actions
      - 2 GB package storage
      - 20GB codespace storage/month
      - 180 hours codespace/month
      - Advance tools and insights in private repos
          - Required PR reviewers
          - Multiple PR reviwers
          - *Draft PR*
          - Protected branches
          - *Code owners* 
          - Auto-link references
          - Github pages
          - Wikis
          - Repos insights graphs
          - Scheduled reminders
          - option to enable/disable codespaces

    **Github Enterprise**
      - Github Enterprise Cloud (hosted on Github.com)
      - Github Enterprise Server (Self hosted)
        
      Features :
      - Everything from Github Organizations team
      - Github Enterprise support w/ SLA
      - Additional security, compliance and deployment controls
      - Authentication with SAML sign-on  
      - Access provisioning with SAML or SCIM (ex: MS Entra ID )
      - Deployment protection for private and internal repos
      - Github connect
      - Options to purchase Advance security
      - 50 K minutes/month of Github Actions
      - 50 GB github package storage
      - 99.99 % montly uptime SLA
      - Central manage policy and billing for multiple github.com org and enterprise account


2. InnerSource refers to the application of open source practices within an organization. This means the source code remains private within the organization, but the development process adopts the open source model. Conversely, with OpenSource, the source code is publicly available with license options.

3. Codespace is exclusively compatible with Linux and **does not** support Windows or Mac operating systems.

4. GitHub Copilot is a tool designed to assist developers by providing autocomplete-style suggestions while they are coding. It analyzes the context within the file being edited and related files, offering helpful suggestions directly within the text editor.

5. By using Github CLI and the Github GraphQL API, one can efficiently handle Github projects without depending on the user interface.

6. A repository owned by a personal account has only two permission levels: Owner and Collaborators.

7. The insights provided by GitHub repository and its respective graphs offer valuable information on traffic, dependent projects, contributors, commits, forks, and network activity. Users with WRITE or ADMIN access to the repository can leverage the Insights feature to generate both **current** and **historical charts**.

8. GitHub Actions is a platform for continuous integration and continuous delivery (CI/CD) that enables automation of build, test, and deployment pipelines. Workflows can be created to build and test every pull request in your repository, or to deploy merged pull requests to production.

9. When following organizations on GitHub, users will be able to view their public activity on their personal dashboard. This includes new discussions, sponsorships, and repositories.

10. GitHub milestones are purpose-built to effectively organize and monitor related issues, enhancing tracking and reporting capabilities.

11. Any individual with **write access** to the repository has the ability to assign issues and pull requests.

12. Gists are essentially Git repositories, allowing you to fork or clone any gist, regardless of whether you are the original author. Additionally, you have the ability to view a gist's complete commit history, along with the differences.

13. You have the option to set up two-factor authentication (2FA) by utilizing a TOTP app on your mobile device or desktop, or through text message. Once you have completed the setup for 2FA using a TOTP app or via text message, you can also incorporate security keys as alternative 2FA methods.

14. Github codespaces are Cloud Developer Environment (CDE) integerated with your github Repo
    - A codespace runs in Ubuntu Linux Docker Container in a VM hosted and managed by Github
    - GitHub Codespaces are designed to be automatically deleted after they have been stopped and remained inactive for 30 days by default. However, it's important to note that Codespaces persist beyond 24 hours of inactivity, and they are not automatically terminated after that duration. In such cases, you might find them in a stopped state and only incur storage costs without CPU costs.
    - New codespace requires - The repo, The branch, The Region and Machine Type to choose 
    - you can view all existing codespaces http://github.com/codespaces
    - Default idle timeout is 30 minutes (maximum is 4 hours)
    - Default retention time is 30 days.
    - Life cycle - Create - Running - STOP ---> Timeouts (can also rebuild if you change dev container)

15. When transitioning the visibility of a code repository from public to private, GitHub will cease to include the repository in the GitHub Archive Program.

16. Members of a team with the *security manager role* have only the permissions required to effectively manage code security for the organization. 
    - Read access on all repositories in the organization, in addition to any existing repository access
    - Write access on all security alerts in the organization 
    - The ability to configure code security settings at the organization level 
    - The ability to configure code security settings at the repository level

17. You have the opportunity to access your codespaces through your web browser, Visual Studio Code, the JetBrains Gateway application, or by utilizing GitHub CLI.

18. A Runner is a pivotal component that undertakes the execution of tasks within the GitHub Actions workflow. It facilitates the essential environment for job execution, enabling workflows to operate across diverse platforms and configurations. Your workflow comprises one or more jobs that can be executed sequentially or concurrently. Each job will be executed within its dedicated virtual machine runner or container and encompasses one or more steps, which either execute a script defined by you or run an action - a reusable extension designed to streamline your workflow.

19.  A job consists of a series of steps within a workflow that is carried out on the same runner. Each step can be either a shell script to execute or an action to run. The steps are executed sequentially and are interdependent. As each step runs on the same runner, it allows for data sharing between steps. For instance, you could have a step dedicated to building your application followed by another step focused on testing the built application.

20.   - **Repository** Represents the logical container holding codebase
      - **Commit** Represents a change in data in the local repository
      - **Remote** A version of your project hosted elsewhere, used for exchaning commits
      - **Branch**: A parallel version of your code that is contained within the repository but does not affect the primary or main branch.
      - **Clone**: To download a full copy of a repository's data from GitHub.com, including all versions of every file and folder.
      - **Fork**: A new repository that shares code and visibility settings with the original "upstream" repository.
      - **Merge**: To take the changes from one branch and apply them to another.
      - **Pull request**: A request to merge changes from one branch into another.
      - **Remote**: A repository stored on GitHub, not on your computer.
      - **Staging Files** Prepares and organizes the changes for the commit 
      - **Upstream**: The branch on an original repository that has been forked or cloned. The corresponding branch on the cloned or forked branch is called the "downstream."

21. A Codespaces deep link is a URL that directly opens a pre-configured GitHub Codespace, containing information about the development environment, extensions, and settings.


22. Code owners are automatically requested for review when someone opens a pull request that modifies code that they own. Code owners are *not* automatically requested to review draft pull requests.

23. | Issues |  Discussion | Pull Requests
| --- | --- | --- | 
| Tracking tasks, bugs, enhancements and other actionable items | Facilitating conversations and Q&As about wide range of topics related to the project| Proposing , reviewing, and merging code changes into the codebase
| <ul><li>often linked to code chanages</li><li>can be linked to **PRs**</li></ul> | <ul><li>Categoized by topics</li><li>Can be *converted* to issue</li><li>Not directly linked to code changes</li></ul></ul> | <ul><li>Directly linked to code changes</li><li>Can be linked to issues</li></ul>

24. A project is adaptable view that can be changed at anytime between 
    - Spreadsheet (table)
    - Taskboard (board)
    - Roadmap (Roadmap)

25. Projects vs Projects Classic 
  Github Projects | Github Projects *Classic*
   | --- | --- | --- | 
   | New , more dynamic interface with tables, boards and views | Traditional board view similar to trello
   | Highly customizable with different views and fields | Limited customization options
  | Supported automated workflows and field updates | Basic automation capablities
  | Enhanced reporting features and insights | Basic reporting and tracking
| Deeper integeration w/ github issues and PR | basic integeration with repos

26. Built-in Project Workflows -automate what happens on specific events 
    - Item added to project
    - Item reopened
    - Item closed
    - Code changes requested
    - code review approved
    - PR merged
    - Auto-archieve items
    - Auto-add to project 
27. Three basic default issue templates 
    - Bug Report
    - Feature Request
    - Custom Template
28. Default Filters in Issues 
    - Your issues
    - Your PR
    - Everything assigned to you
    - Everything mentioning you

29. Gists are provide a simple way to share code snippets with others. Every gist is a git repository, they can be forked or cloned.
    - Gist can be public or secret 
        - Public Gists are searchable. 
        - Public Gists show up in Discover
            - https://gist.github.com/discover
        - Secret gists are not searchable and do not show up in discovery
        - Secret gists are **NOT** private 
            - you can share the URL with friends
        - Secret gists can be changed to be public
        - Public Gists **cannot** be changed to private
        - You can pin gists to your profile and others to easily find 
        - Giss allow others users to comment
        - Gists allow you to easily navigate revisions
        - 
30. Github Repo has multiple features we can *enable or disable*
     - Wikis
     - Issues
     - Sponsorships
     - Preseve this repo
     - Disucssions
     - Projects
     - ..more
  
31. Repository Permission Levels 
    - **READ** - Can read and clone this repository. Can also open and comment on issues and PR
    - **TRIAGE**  can read and clone this repository. Can also also manage issues and PR
    - **WRITE** Can read, clone and push to this to repository. Can also manage issues and PR
    - **MAINTAIN** - can read, clone, push to this repo. Can also manage issues and PR, and some repository settings
    - **Admin** - Can read, clone, push to this repo. Can also manage issues and PR, and  repository settings including adding collaborators
    - Enterprise allow custom roles 
    - 
32. Branch Protection Rules:
    - Require a PR before merging
    - Require status checks to pass before merging
    - Require conversation resolution before merging
    - Require signed commits
    - Require linear history
    - Require deployments to succeeed before merging
    - Lock branch
    - Do not allow bypassing the above settings
    
    Rules applied to everyone including administrators to avoid force pushes /deletions 