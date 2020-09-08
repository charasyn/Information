## 1. Github Repository Branches:star:
Often, we need to add features and functionalities to our existing programs. There is always a significant risk of breaking the current working solution while adding these features. Git provides a feature to develop and experiment with the new features before merging into the operational master branch. As similar to its name, a 'branch' is the parallel version of the repository development's mainline. As mentioned earlier, branches are mostly used to develop features, fix bugs, and experiment with new ideas.
In the below tutorial, we will cover both the command-line instructions and Web-UI instruction to perform tasks related to branching.

- ## Creating a new branch 

For the web-application:


Once the repository is created, click on the repository's name from the list to go inside it. As provided below, click on the "master" dropdown, and an option will appear: find or create a new branch. Add the branch's name in the textbox and then click on the option below the textbox "Create branch: <branchname> from masters." After clicking that option, you will be automatically redirected to the intended branch. Feel free to play around inside your branch without affecting the content in master.

<p align="center">
  <img width="700"  src="images/Branch_Creation.PNG">
</p>

For command-line:

We can use the below command to create a new branch.
```
git checkout -b <branchname>
```
where -b tells checkout to create a new branch

If you need to confirm the current branch you are using, try the below command.
```
git branch
```
To link the newly created branch to Github, use the below command.
```
git push -u origin <branchname>
```
You can make your experimental changes to any of the content inside the branch.


- ## Checking differences between different branches (branches and master)

For the web-application:

In the below example, I created a branch (Test_branch) and added a file "test.md" which is not present in the master. In order to check the difference, click on the compare option which is at the right-upper corner as indicated in the below screeshot.

<p align="center">
  <img width="700"  src="images/Diff_branch.png">
</p>

As indicated below, the branch has been changed with 1 addition (test.md) and 0 deletion. 

<p align="center">
  <img width="700"  src="images/Diff_branch_res.png">
</p>

For command-line:

To view the difference between the current branch and the 'master' branch. Use the below command.
```
git diff master
```

If 'git diff' is used by itself (with no following parameter), it will show us differences from the most recent commit.
We can also use git diff with a commit identifier to see the differences between
the current version and a specified commit or with two commit identifiers to see the
differences between two specific commits.
If you need to find difference with a specific file, add the file name at the end of the commment.

- ## Merging the branches

The branches can be merged with the master once the developemt is complete in the brancher. Use the below command in order to execute this task. We need to check out the master branch and then merge the branch. At the end, the merged master branch needs to pushed to GitHub.

```
git checkout master
git merge <branchname>
git push
```

- ## GitHub pull requests

**Creating a pull request**


Pull requests help you to notify your teammates about changes you've pushed to a GitHub repository. Once a pull request is sent, interested parties with required access can review the set of changes, discuss potential modifications, and even push follow-up commits if necessary. When you are inside a specific branch, you can submit a pull request by clicking on the "Pull request" button. 

<p align="center">
  <img width="700"  src="images/Pull_req1.PNG">
</p>
After clicking the button, you will be taken to another screen where you can write/upload details about your pool request. Finally you can click on the "Create pull request" button to complete the process of creating the pull request.

<p align="center">
  <img width="700"  src="images/Pull_req2.PNG">
</p>

Once the pull request is submitted, you can find it by clicking on "Pull request" tab located at the homepage of that specific repository.

<p align="center">
  <img width="700"  src="images/Pull_req3.png">
</p>

**Using a pull request**


You can write comments related to a pull request, view all the commits by all contained by a pull request under the commits tab,
or see all the file changes from the pull request across all the commits under the "Files Changed" tab. You can event leave a comment on particular lines in the code change simply by hovering to the left of a line and clicking on the blue note icon. All these options can be found in the "Pull request" tab as mentioned in the above section.

**Merging a pull request**


Once you finalize the changes , you can merge the changes back to master. There are a few ways to do this.

First, you can use github's "Merge pull request" button at the bottom of your pull request to merge your changes. This is only applicable when there is no merge conflict with the base branch. If no conflict,  you just have to add a commit message and click on "Confirm Merge" to merge the changes.

<p align="center">
  <img width="700"  src="images/Merge_pull.png">
</p>

After you successfully merge the branch to the master, you will be seeing an option to keep or delete the branches.
If the pull request cannot be merged online due to merge conflicts, or you want to perform some experimentation locally before sending the merge to the repo on Github, you can perform the merge locally instead. 

In long standing branches, merging can often cause lots problems when updating if changes in a given branch conflict with changes recently merged into the master branch. If there are many commits to the same file, git merge may force you to fix the same merge conflicts over and over again. While there are several ways to mitigate this issue, such as enabling git rerere to reuse recorded resolution of conflict merges, squashing a series of related changes into 1 commit and cherry-picking it into the master is a great solution, especially for topic branches and isolated features.

There are several advantages of these methods. First, you only have to deal with merge conflicts once. Second, each commit represents an entire set of changes required for a feature or task, which makes it easy to pin point bugs and other problems when they arise and to remove a change set when it's no longer necessary.

Github recently introduced these options (squash, rebase) online to handle conflicts efficiently and they also provide a detailed instructions on merging the pull request through the command line. The options are indicated in the below screenshots.

<p align="center">
  <img width="700"  src="images/Merge_pull_opt.png">
</p>

- ## Deleting the branches

TO delete the branch from the local machine, use the below command.

```
git branch -d "branchname"
```
To delete the branch on Github, we need the following two commands.

```
git push origin --delete "branchname"
git remote prune origin
```

## 2. Github Repository Tagging:star:

Tagging in git refers to creating specific points in history for your repository and data. Tagging is usually done to mark release points of the stable version of your code.
To create a tag, firstly check out the branch where you want to create the tag. To checkout the current branch use the below command.
```
git checkout <branch name>
```

Then create a tag and give it a name. 

```
git tag <tag name>
```

To verify if the tag is already created, use the below command.
```
git tag
```

To create an annotated tag, use the below command.

```
git tag -a v1.0 -m "creating version 1.0"
```

To check the details of a specific tag, use the below command

```
git show <tag name>
```

To push the tag to the github (remote), use the blow command.
```
git push origin <tag name>
```

To push all the tags at once, use the below commands.
```
git push origin --tags
```
To delete the tags from the local, use the bolow commands
```
git tag -d <tag name>
or 
git tag --delete <tag name>
```
To delete the tags from the remote, use below commands.

```
git push origin -d <tag name>
or
git push origin --delete <tag name>
or
git push origin :<tag name>
```
To delete multiple tags at once, use the below commands

```
git tag -d v1.0 v1.1 (local)
git push origin -d v1.0 v1.1 (remote)
```

We cannot directly checkout tags in github. We can create branch from a tag and checkout the branch. Follow the bolow command in order to execute the process.
```
git checkout -b <branch name> <tag name>
```

We can also create a tag for past commits using the below command.

```
git tag <tag name> <reference of commit>
```
where the reference number is the checksum associated with the commit. The history of commits and checksum number can be accessed through "git log" command.

