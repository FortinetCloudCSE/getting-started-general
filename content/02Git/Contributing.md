---
title: "Contributing"
menuTitle: "Contributing"
weight: 50
---

Git is primarily a code versioning system used to facilitate development collaboration amongst teams of developers. Git workflows can get pretty complex, and the purpose of this document is to provide an overview of simple workflows and Git commands that can be used for branching and pushing code and working with repositories.

If you'd like to dive deeper on Git, the official documentation can be found here: [https://git-scm.com/docs](https://git-scm.com/docs)

Atlassian also provides a series of very accessible tutorials here: [https://www.atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials)

### Git branching

It is advisable to create a new branch in each repo to work with, distinct from the main branch. A suggested naming convention is **Feature-username-reponame", substituting in your Git username and the name of the repo for username and reponame, respectively. The following commands, when issued from within a local directory holding the repo, will create a new branch to work with:

```shell
git checkout -b Feature-username-reponame
```

This enables one to work on the repo and test changes while maintaining the main branch in a consistent, working state. 

For further details on Git Workflow guidelines, please see our workshop documentation [here](https://fortinetcloudcse.github.io/UserRepo/03chapter3/3_task2.html) and [here](https://fortinetcloudcse.github.io/UserRepo/03chapter3/gitflow.html).

