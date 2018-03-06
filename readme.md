# Automatic branch tracking for project in Danske Spil's JIRA

If you setup your project as described here, it will allow your team to use Branches and Pull Requests in your source-code repositories to automate the transition of issues in JIRA.  Specifically
- When you create a new branch for an issue/feature, the corresponding issue will automatically transition to **IN PROGRESS** in JIRA.
- When you create a new pull request for a branch, the issue will transition to **IN REVIEW**.
- If a pull request is rejected, then the issue will transistion back to **IN PROGRESS**.
- When a pull request is merged back into *master*, the issue will transition to **DONE**.

There are basically two routes, depending on whether you have an existing project or are creating a project from scratch.

- [Creating a new JIRA project](new-project/new-project-in-jira.md).
- [Automating an existing JIRA project](existing-project/existing-project-in-jira.md).

After you have setup your project, you can make the issues transition automatically be [using branches](../using-branches/using-branches-to-control-issues.md) in your project repository.

This is part of a [greater effort](https://jira.danskespil.dk/jira/browse/DEVOPS-388) to get better release reports.

The initial automation setup is [described elsewhere](big-bang/start-from-scratch-automation-jira.md).
