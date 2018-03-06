# Creating automated workflow for a JIRA project

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

Continue and create the rest of the triggers so that *Pull Request Created* and *Pull Request Merged* are use to transition issues:

![Create project 19](new-jira-project-19.png)
![Create project 20](new-jira-project-20.png)
![Create project 21](new-jira-project-21.png)
![Create project 22](new-jira-project-22.png)

Now your project will have triggers on the workflow, so that you can make the issues transition automatically be [using branches](../using-branches/using-branches-to-control-issues.md) in your project repository.

To set up a Scrum board, see [setting up a new project](../new-project/new-project-in-jira.md#make-a-scrum-board).
