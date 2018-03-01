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

Clone the repo, create a readme, and push it back to get started.  I do it this way, YMMV.

![Create new repo 4](new-repo-4.png)

![Create new repo 5](new-repo-5.png)

# Create new project

Log in to [JIRA](https://jira.danskespil.dk), and Create a project with shared configuration.

![Create project 1](new-jira-project-01.png)

![Create project 2](new-jira-project-02.png)

Use the Standard Development Project:

![Create project 3](new-jira-project-03.png)

The *Key* of the project is import because that is what will be used to link JIRA issues to branches in Git.  JIRA will suggest one for you:

![Create project 4](new-jira-project-04.png)

# Make a Scrum board

Create a board for your project, for instance a Scrum board:

![Scrum board](scrum-1.png)

![Board](scrum-2.png)

Give the board a name that relates it to the project (because there are many boards in our JIRA):

![Backlog](scrum-3.png)

The vanilla board is very simple, so you might want to add an extra column for In Review:

![Simple Board](scrum-4.png)

![Simple Backlog configuration](scrum-5.png)

Add a column to the board, and drag the IN REVIEW status to the In Review column:

![Review Column](scrum-6.png)

That is it, now you have a new Scrum project that automatically tracks feature branches in you Git repository.

