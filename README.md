# Assignment Submission Instructions
[![HitCount](http://hits.dwyl.io/Naereen/badges.svg)](http://hits.dwyl.io/Naereen/badges)

Created By: Matt Dixon, Cesur Kavaslar, Steven Ding

## 1. Create GitHub account
Many of you may already have a GitHub account, if you do you can skip this step. If you don’t have an account, go to github.com and create one.

We recommend you choose the free plan for this course. You are able to skip all steps until you are asked to verify your email address.

After verifying our email, you will be brought to your hello-world repository. 

## 3. Where to ask question?
There is an `issues` tab right up there :point_up:. Cannot find it? Click <a href='https://github.com/CISC-CMPE-327/Assignment-Instructions/issues'>HERE</a>. To ask a question, follow two steps:

- Frist, search for related issue using the `Filters` box. 
- If no one asked before, create an issue with a title that summazie your whole question. Then fill in the body of your question. You can copy screenshot and parse into the text box as well. 

## 2. Add Education License
Go to https://education.github.com/discount_requests/new and add your Queen’s email to receive GitHub’s Education benefits for free.

You will be asked to verify the account in Email Settings. Once the address is verified, your benefits should be accessible.
Create a Private GitHub Repository
Now that you have an account, you can create your repository (repo) for the course. Only one person per group needs to create a repo. 

Navigate to your repositories page and click the green button in the upper-right labeled “New” to create a new repo. 


Name your repo (we suggest Quinterac) and make sure to change your repo to Private. As well, you’ll want to initialize your repo with a README file and add the license you chose for your project in Assignment 0.


## 3. Add Collaborators
Go to the Settings tab of your new repository and select the Collaborators option on the left.
 
First, add each of your team members’ GitHub Accounts as  collaborators to the repo.
Next, add each of the TA’s accounts as collaborators as well - this will allow us to mark your assignments.
steven-hh-ding
mattdixon97
cesurk
Ghazall1993
Andrew
combly
Congratulations, you’ve finished setting up your repo and now it’s time to start working! If you are unable to add more than 3 collaborators, make sure that you have added in your educational license in the 2nd step.

## 4. Sign up GitHub Actions (for Continuous Integration):
With GitHub Actions, you will be able to automatically run all your test cases directly on the cloud, whenever you make changes to your codebase. Sign up Github Actions by going to the link below and click `sign up for the beta`.
https://github.com/features/actions

Following the instruction and you will be able to use GitHub Actions for your course project. You will have 2,000 minutes test runtime per month for your project. You will find that at your repository homepage there is now one additional tab ‘Actions’. You will be able to find all the logs of all the test runs, and where it broke: 




Setting up GitHub Actions workflow for your project is simple. Since this is relatively new, we have setup a list of minimal template repositories for different languages here https://github.com/CISC-CMPE-327. You can start to structure your project from there. The xxx.yml file in the folder `.github/workflows` define the workflow of your CI process. Different language uses different toolchains so please find your template according.  But typically:


name: the name of your CI process. Can be anything. You name it.
on: the event for which will trigger your CI process. Here we add push. Means that everytime you push your code to the repository, it will trigger the script to run!
runs-on: which platform you would like the test case to run on.
steps: steps to carry out in sequence.
uses: leverage existing operations defined in github actions. In this example, `actions/checkout@v1` means downloading the code.
name: give a name to a step. Usually under the name item you will find a `run` item.
run: the script/command to execute

These templates provide you a starting point to setup your repository and understand how the workflow works for GitHub Actions (well the other CI platforms all follow a similar idea, under the hood GitHub Actions uses M$ Azure pipelines). You are free to organize the file and test cases in any ways that you prefer. Just be sure to document them accordingly. 

The ‘passing’ badge on the homepage (in the README file) still points to the original template. So make sure that you update the link accordingly pointing to your repository. 


## 5. Clone the Repository to Your Laptop
git clone …



## 6. Committing changes to Github
First: make sure that you are working on the master branch 
git branch -a



git pull 


git add all …
git commit -m ...
git push



## 7. Creating a Tag for Assignment Submission



## 8. Create

