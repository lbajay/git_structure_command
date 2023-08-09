# Git Branching Strategy & Naming Convention

## Description

Git offers flexible branching strategies, a branching strategy is a set of rules, a convention that helps teams and developers – they can follow rules and conventions to create a new branch, its flow, etc.

Git branching strategies allow separation of work. Broadly, we can divide Git branches into two categories: Regular & Temporary Branches.

### Regular Git Branches

These branches will be available in repository on permanent bases. Their naming convention is simple and straightforward.

- Development (dev) is the main development branch. The dev branch’s idea is to make changes in it and restrict the developers from making any changes in the master branch directly. Changes in the dev branch undergo reviews and, after testing, get merged with the master branch.

- Master (master | main) is the default branch available in the Git repository. It should be stable all the time and won’t allow any direct check-in. You can only merge it after code review. All team members are responsible for keeping the master stable and up-to-date.

- QA (QA), or test branch, contains all the code for QA testing and automation testing of all changes implemented. Before any change goes to the production environment, it must undergo the QA testing to get a stable codebase.

### Temporary Git Branches

As the name indicates, these are the branches that can be created and deleted when needed. They can be as follows:

- Feature Branches (feature)
- Bug fix (bugfix)
- Hot fix (hotfix)
- Experimental Branches (experiment)
- WIP (Work In Progress) branches (wip)

#### Start branch name with a Group word

It is one of the best practices. The group word can be anything to match workflow.

- Feature - The feature which will be implemented
- Bug – The bug which needs to be fixed soon
- Hotfix - Something which needs to be fixed ASAP
- Experiment - This will be created for experiment purpose
- WIP – The work is in progress, and aware it will not finish soon

### Naming Convention of Branches

```
feature/branch-name
bugfix/branch-name
hotfix/branch-name
experiment/branch-name
wip/branch-name
```

#### Use Unique ID in branch names

You can use the issue tracker ID in your branch name. The name shows that the branch applies to the task of adding a testing module, the tracking ID of the issue is 8712, and the work is in progress.

One more advantage of using an external tracking ID in the branch name is the possibility to track the progress from an external system.

```
wip-8712-add-testing-module
```

#### Use Hyphen or Slash as Separators

Many developers use slash as a separator, and many use hyphens. Which one to use depends on the team’s preferences.

My opinion is that hyphens make the name more comfortable to read, so it’s a suitable separator in branch names. You can use slashes, hyphens, and underscores. The point is to be consistent.

### Review and merge code with pull requests

- Two reviewers are required, an optimal number based on requirements.
- Take care of assigning the same reviewers to a large number of pull requests.
- Pull requests work better when reviewer responsibilities are shared across the team.
- Provide enough detail in the description to quickly bring reviewers up to speed with your changes.

### Release branches

- Create a release branch from the main branch
- Branch close to release time or other milestones, such as the end of a sprint.
- Give a branch name associating it with the release, for example: release/0.0
