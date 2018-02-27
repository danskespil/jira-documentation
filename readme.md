# How to create a new development project in Danske Spil's JIRA

Creating a project as described here will allow your team to use Branches and Pull Requests in your source-code repositories to automate the transition of issues in JIRA.  Specifically
- When you create a new branch for an issue/feature, the corresponding issue will automatically transition to *IN PROGRESS* in Jira.
- When you create a new pull request for a branch, the issue will transition to *REVIEW*.
- If a pull request is rejected, then the issue will transistion back to *IN PROGRESS*.
- When a pull request is merged back into *master*, the issue will transition to *DONE*.

This is part of a [greater effort](https://jira.danskespil.dk/jira/browse/DEVOPS-388) to get better release reports.

# Create new repository

Start with creating a repository for the source code.  That way JIRA have time to pick up on the existence of the repository.

Go to [Bitbucket](https://bitbucket.org/dsintegration/) and create a new repository:

![Create new repo 1](new-repo-1.png)

![Create new repo 2](new-repo-2.png)

![Create new repo 3](new-repo-3.png)

Clone the repo, create a readme, and push it back to get started.

![Create new repo 4](new-repo-4.png)

![Create new repo 5](new-repo-5.png)

# Create new project

Log in to [JIRA](https://jira.danskespil.dk), and create a Basic Software Development project to get the proper basic workflow.  Don't worry, we will make it Scrum or Kanban later, but we have to start this way.

![Create project 1](new-jira-project-01.png)

![Create project 2](new-jira-project-02.png)

![Create project 3](new-jira-project-03.png)

The *Key* of the project is import because that is what will be used to link JIRA issues to branches in Git.  JIRA will suggest one for you:

![Create project 4](new-jira-project-04.png)

After the project is created, you will need to setup the workflow:

![Create project 5](new-jira-project-05.png)

![Create project 6](new-jira-project-06.png)

The JIRA interface for editing the workflow is somewhat unituitive.  It displays different things depending on whether your are in edit mode or view mode, and whether your are in diagram mode or text mode.

When you click to edit on the workflow, you will be prompted your password to switch to administrator role.

![Create project 7](new-jira-project-07.png)

![Create project 8](new-jira-project-08.png)

To put triggers on the workflow, you need to be in diagram mode:

![Create project 9](new-jira-project-09.png)

Click on the *IN PROGRESS* transition to get a menu to the right:

![Create project 10](new-jira-project-10.png)

Click *triggers*:

![Create project 11](new-jira-project-11.png)

And *Add Trigger*:

![Create project 12](new-jira-project-12.png)

Specifically a *Branch Created* trigger.

![Create project 13](new-jira-project-13.png)

![Create project 14](new-jira-project-14.png)

Now the new trigger should be listed:

![Create project 15](new-jira-project-15.png)

Continue to add one more triggers for sending an issue back to *IN PROGRESS* if a pull request is rejected:

![Create project 16](new-jira-project-16.png)

Then publish the workflow, no need to create a backup:

![Create project 17](new-jira-project-17.png)

![Create project 18](new-jira-project-18.png)



![Create project 19](new-jira-project-19.png)
![Create project 20](new-jira-project-20.png)
![Create project 21](new-jira-project-21.png)
![Create project 22](new-jira-project-22.png)

![Scrum board](scrum-1.png)
![Backlog](scrum-2.png)
