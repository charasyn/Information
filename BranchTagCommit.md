## 1. GitHub Repository Branches:star:
Often, we need to add features and functionalities to our existing programs. There is always a significant risk of breaking the current working solution while adding these features. Git provides a feature to develop and experiment with the new features before merging into the operational master branch. As similar to its name, a 'branch' is the parallel version of the repository development's mainline. As mentioned earlier, branches are mostly used to develop features, fix bugs, and experiment with new ideas.
In the below tutorial, we will cover both the command-line instructions and Web-UI instruction to perform tasks related to branching.

## - Creating a new branch 

For the web-application:


Once the repository is created, click on the repository's name from the list to go inside it. As provided below, click on the "master" dropdown, and an option will appear to find or create a new branch. Add the branch's name in the textbox and then click on the option below the textbox "Create branch: 'branchname' from masters." After clicking that option, you will be utomatically redirected into the intended branch. Feel free to play around inside your branch without affecting the content in master.

<p align="center">
  <img width="700"  src="images/Branch_Creation.PNG">
</p>

For command-line:

We can use the below command to create a new branch.
```
git checkout -b *branchname*
```
where -b tells checkout to create a new branch

If you need to confirm the current branch you are using, try the below command.
```
git branch
```
To link the newly created branch to GitHub, use the below command.
```
git push -u origin *branchname*
```
You can make your experimental changes to any of the content inside the branch.


## - Checking differences between different branches (branches and master)

In the below example, I created a branch (Test_branch) and added a file "test.md" which is not present in the master. In order to check the difference, click on the compare option which is at the right-upper corner as indicated in the below screeshot.

<p align="center">
  <img width="700"  src="images/Diff_branch.png">
</p>

As indicated below, the branch has been changed with 1 addition (test.md) and 0 deletion. 

<p align="center">
  <img width="700"  src="images/Diff_branch_res.png">
</p>

