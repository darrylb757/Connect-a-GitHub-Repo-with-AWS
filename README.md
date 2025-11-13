# Connect-a-GitHub-Repo-with-AWS
I will set up a Git repository for my web app's code. By the end of this project, the code that I wrote for my Java web app will be store securely in GitHub.
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Connect a GitHub Repo with AWS

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-github)

**Author:** Darryl Brown  
**Email:** darrylbrown1991@gmail.com

---

## Connect a GitHub Repo with AWS

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_dd9d254e)

---

## Introducing Today's Project!

Today in this project I will set up a Git repository for my web app's code. By the end of this project, the code that I wrote for my Java web app will be store securely in GitHub.

### Key tools and concepts

Services I used were Github, Amazon EC2, Keypairs, and VS Code. Key concepts I learnt include setting up Git repo, difference between Git and Github, commands for staging, saving, and pushing changes. Also upstream repos, setting up a remote origin, and branches.

### Project reflection

This project took me approximately 1hr. It was most rewarding to dive into Github and Git and learning the different repo commands. 

I did this project to learn more about Git and Github. This is also day 2 of 7 day Devops projects where I will continue to fulfill these challenges and keep learning. 

This project is part two of a series of DevOps projects where I'm building a CI/CD pipeline! I'll be working on the next project shortly.

---

## Git and GitHub

Git is Git is like a time machine and filing system for your code. It tracks every change you make, which lets you go back to an earlier version of your work if something breaks. I installed Git using the commands 
sudo dnf update -y
sudo dnf install git -y


Look at GitHub as a storage space for different version of your project that Git tracks. Since GitHub is a cloud service, it also lets me access my work from anywhere and collaborate with other developers over the internet. I'm using GitHub in this project to help use Git and see my file changes in a more user friendly way. It's just like how using an IDE (VSCode) makes editing code easier.

GitHub is also especially useful in situation where you're working in teams and need to share your updates and reviews to a shared code base.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_efaadbf7)

---

## My local repository

A Git repository is are folders that contain all your project files and their entire version history. Hosting a repo in the cloud, like on GitHub, means I can also collaborate with other engineers and access your work from anywhere.

Git init is a command that initializes in your local repository. When you run git init inside a directory e.i. nextwork-web-project where I ran mine. it sets up the directory as a local Git repository which means changes are now tracked for version control.

A branch in Git is like alternate universes of the same project. For example, if you wanted to test a change to your code, you can set up a new branch that lets you diverge from the original/main version of your code (called master) so you can experiment with new features or test bug fixes safely. After running git init, the response from the terminal was yellow text is just Git giving you a heads-up about naming your main branch master and suggesting that you can choose a different name like 'main' or 'development' if you want.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_7bf21bae)

---

## To push local changes to GitHub, I ran three commands

### git add

The first command I ran was " git add . " . Which adds changed to staging area. A staging area in Git is a place to review all changes made to code so you can decide what changes to make.

### git commit

The second command I ran was Git commit. Is for saving changes in staging area. Using -m in that command also leaves us messages for changing that commit.

### git push

The third command I ran was Git push. This command pushing code changes to remote origin. Using '-u' is a special feature in the command that makes our remote origin the default upstream for the local branches. Telling Git to remember to push to master branch by default.

---

## Authentication

When I commit changes to GitHub, Git asks for my credentials because Git needs to double check that you have the right to push any changes to the remote origin your local repo is connected with.

### Local Git identity

Git needs my name and email because it is a version control system, it is used for tracking changes to code. To really identify who made what changes. 

Running git log showed me that by default, Git is saving our code changes to a username called ec2user instead of actual name and details. 

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_9a27ee3b)

---

## GitHub tokens

GitHub authentication failed when I entered my password because GitHub phased out password authentication to connect with repositories over HTTPS - there are too many security risks and passwords can get intercepted over the internet.

A GitHub token is a temporary password that grants access to github account. I'm using one in this project because it lets me safely authenticate to my github repository while using this EC2 instance.

I could set up a GitHub token by navigating to developer settings in github and set a custom expiration date with only repo permissions.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_fa11169d)

---

## Making changes again

I wanted to see Git working in action, so I made another change to index.jsp file. I couldn't see the changes in my GitHub repo initially because I didn't add, committed, or pushed those changes. 

I finally saw the changes in my GitHub repo after running the same three commands and then refreshing index.jsp my Github repo.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_6becb2bc)

---

## Setting up a READMe file

As a finishing touch to my GitHub repository, I added a README file, which is a document that introduces and explains my project, like what the project does, how to set it up, and how to use it. I added a README by running touch README.md, I've just created a new blank file with the name README.md. file by touch is Linux command for creating a new file.

My README is written in Markdown because it lets me format text that I'll display on my webpage. With Markdown, I can make words bold, create headers, add links, and use bullet points. 

My README file has 5 sections that outline my project.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-devops-github_c94976902)

---

---
