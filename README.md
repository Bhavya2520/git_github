# git_github
This repository serves as a comprehensive guide to understanding Git and GitHub, curated for learning purposes. It covers everything from the basics of version control to more advanced Git operations, making it ideal for beginners and intermediate users alike.
# Git & GitHub Notes

## What is Git?
Git is a free and open-source distributed version control system that manages everything GitHub-related locally on your machine.

## 🚀 Git Repository Initialization (Step-by-Step Guide)

Follow these steps to initialize your Git repository and push your code to GitHub:

```bash
# Step 1: Initialize Git in your local project
git init
# This creates a hidden .git folder in your project directory that stores all version control info.

# Step 2: Add files to the staging area
git add .
# Stages all files in the current directory.
# You can also stage a specific file using:
git add <filename>

# Step 3: Commit the staged changes
git commit -m "Initial commit"
# Commits the staged snapshot with a descriptive message.

# Step 4: Add the remote GitHub repository URL
git remote add origin https://github.com/your-username/your-repo.git
# Replace with your actual GitHub repo URL.

# Step 5: Verify the remote URL
git remote -v

# Step 6: Push code to the main branch on GitHub
git push origin main
# Use 'main' or 'master' depending on your default branch.

```



## 1) What are the other platforms same as GitHub to version and maintain your code?
Platforms like GitHub that are used for version control, code hosting, and collaboration:
# Git Hosting Platform Comparison

| Platform        | Best For                                      |
|-----------------|-----------------------------------------------|
| **GitHub**      | Open-source, community, and collaboration     |
| **GitLab**      | DevOps in one place                           |
| **Bitbucket**   | Jira/Atlassian users                          |
| **SourceForge** | Older open-source projects                    |
| **CodeCommit**  | AWS users                                     |
| **Azure Repos** | Microsoft/Azure ecosystem                     |


## 2) `git init`
- It creates a hidden folder named `.git` in your directory.
- This `.git` folder contains all the metadata (version history, configs, logs, etc.) required to track changes in your code.

## 3) What is inside the `.git` folder?
<img width="768" height="537" alt="image" src="https://github.com/user-attachments/assets/b8d8f74c-d93e-4e54-bd90-931286bc4257" />

## 4) What is the use of the `git status` command?
The `git status` command is used to check the current state of your working directory and staging area. 
<img width="598" height="255" alt="image" src="https://github.com/user-attachments/assets/bd47a8d7-d78f-432c-a08b-8a539626eb14" />

Useful for if any changes are made after the git commit (modified file tracks).

## 5) Use of `git add .`
- Stage all changes (new files, modified files, and deletions) in the current directory and subdirectories for the next commit.
- <img width="914" height="196" alt="image" src="https://github.com/user-attachments/assets/1db77456-61b7-47ce-9bff-5c87ff0538ec" />

- For a particular file if you want to add then command is `git add <filename>`

## 6) `git commit -m "new commit"`
The `git commit -m` command is used to save (commit) your staged changes in Git with a message.

## 7) If you want to remove the stage of current file then you write `git restore`
```bash
git restore --staged <filename>
```
<img width="1337" height="255" alt="image" src="https://github.com/user-attachments/assets/e6c24868-0277-44cf-99ed-b0f08c0984db" />
<img width="1029" height="625" alt="image" src="https://github.com/user-attachments/assets/75feafbe-42e7-43f8-a682-e5614b301ba0" />

## 8) `git log`
The `git log` command is used to view the history of commits in a Git repository.
<img width="698" height="323" alt="image" src="https://github.com/user-attachments/assets/722a45f6-ff81-45ec-a4a8-bc3ad76b0ab4" />


## 9) If you want to remove the last commit because the file has been deleted by mistake then how can you do it?
<img width="533" height="421" alt="image" src="https://github.com/user-attachments/assets/58f27848-3d34-40c1-9136-ed491ba2b7eb" />

Suppose here you want to delete last two commits then:  
Then copy the hash before that last two commits.  
<img width="975" height="145" alt="image" src="https://github.com/user-attachments/assets/88e59ca4-547e-4daa-83ea-9932b79bd3d6" />

Then again you check `git log` now you will be only see the one commit.
<img width="768" height="253" alt="image" src="https://github.com/user-attachments/assets/e6c76c32-a8d6-446e-91aa-5527debb0399" />


## 10) Where these all changes has gone?
In the unstaged area.
<img width="701" height="310" alt="image" src="https://github.com/user-attachments/assets/bbae0228-eb1f-43c8-9039-d62fe0f66d76" />


## 11) If you want that your progress or a feature of the project that code you have written,
is there any way so that put your work somewhere else without making a commit and history and whenever you want that things back you get it?  
Command: `git stash`  
<img width="742" height="299" alt="image" src="https://github.com/user-attachments/assets/f7bedfdb-536b-4889-aae9-b407ee299ef8" />
<img width="680" height="445" alt="image" src="https://github.com/user-attachments/assets/855bfdbd-6eeb-40f8-9da2-1415a44ea14b" />
<img width="634" height="416" alt="image" src="https://github.com/user-attachments/assets/ed724abf-f9a5-4012-9267-c1f97e62bc60" />

If you do not want to lose your current status of the git and also do not want that changes in your repo.  
You're just saying: just go back to the stage and when I need I will call for you.
<img width="719" height="417" alt="image" src="https://github.com/user-attachments/assets/1e5b27e3-643c-4b83-8916-d9cee8d1d80c" />


## 12) For calling stash in project folder
Command: `git stash pop`

## 13) If you want to clear or remove the stash which you have stored then
Command: `git stash clear`

## 14) To add project on GitHub repo
Command: `git remote add origin <link of repo>.git`

## 15) If you want to see the link which is associated with this folder then command is
Command: `git remote -v`

## 16) For push code in the repository
Command: `git push origin <branch name_master>`

## 17) How to create a branch
Command: `git branch <branch name>`

## 18) How to change the branch
Command: `git checkout <branchname>`  
Means head is changing towards the branch name that you have provided.

**Note:** Whenever you are creating a new branch at that time the new branch is created from your head is currently pointing.  

Create a new branch with the given name and switch to it immediately:  
```bash
git checkout -b feature1
```

## 19) How to clone the repository which is already exist
Command: `git clone <link>`

## 20) Why we required to clone the repository
Because whenever you are trying to add some code in some organization you did not able to push the code into the directly main repository.  
It is so risky for that organization, so for that first of all you have to fork that repository into your GitHub account.  
After that you can change the code by your own on your repo.

## 21) From where you have forked the repository that is known as upstream URL  
And how to add upstream URL
<img width="975" height="215" alt="image" src="https://github.com/user-attachments/assets/c95ad854-1037-41c7-ac6d-d199abea61e7" />


## 22) If you have created a type of branch separately and add one feature on that and you want to merge that feature on the main branch then how can you do it?
For that you need to create PR request.

**Note:** If one branch is `<main>` and another branch is `<new feature>` then if `<new feature>` branch has made a request to push the code onto the main branch, only one time pull request has been created.  
And after that again if you commit some other things onto the `<new feature>` branch at that time new pull request is not being generated — it is automatically added into the main branch.
<img width="710" height="393" alt="image" src="https://github.com/user-attachments/assets/f7e9c7ef-3dcf-4416-8809-f3ca9a9b2865" />
<img width="975" height="259" alt="image" src="https://github.com/user-attachments/assets/c9701e19-dae9-494d-94ca-fca7bd0748a8" />
<img width="975" height="319" alt="image" src="https://github.com/user-attachments/assets/5ed38693-ac25-470d-9e84-d35226422f04" />




## 23) At a time only one PR is open

<img width="975" height="205" alt="image" src="https://github.com/user-attachments/assets/2b426443-bf85-4550-9785-0843b9103a91" />
<img width="724" height="301" alt="image" src="https://github.com/user-attachments/assets/d7b9d08d-cd65-41d0-8a30-456d10154d44" />
<img width="483" height="394" alt="image" src="https://github.com/user-attachments/assets/d6eb47cf-5fff-49d8-8556-ff11fcd5c06a" />
<img width="975" height="387" alt="image" src="https://github.com/user-attachments/assets/038fd54d-180d-4c24-af92-817c9efac005" />





## 24) But I have confused in that if I feel like I have completed my feature and after the code reviewer says that you have to add these things and I have to add those things into my branch but I have already created one PR for pushing my code already with the main branch — so if I commit the new changes in my branch, that is also reflected on the main branch?
<img width="975" height="506" alt="image" src="https://github.com/user-attachments/assets/d274a527-9b3a-4e59-aff1-03c0683a6b48" />
<img width="975" height="414" alt="image" src="https://github.com/user-attachments/assets/137d4d4e-9e70-4196-8c84-9fa2cdae7493" />


## 25) Merging main branch with my feature branch and after two months the client says that I want these changes in this feature so I have already created PR previously — I have just explained — then I need to change the code or change the new feature — then in that case what should be done
<img width="633" height="466" alt="image" src="https://github.com/user-attachments/assets/ceb79a4e-beed-4837-8125-2a384a245b40" />
<img width="723" height="563" alt="image" src="https://github.com/user-attachments/assets/1dd6e93f-dc70-4915-99a7-60dda0f6ac93" />
<img width="812" height="441" alt="image" src="https://github.com/user-attachments/assets/e53a950a-fbb1-489b-8dd3-450a067a4799" />



## 26)
<img width="785" height="461" alt="image" src="https://github.com/user-attachments/assets/c52bd123-5227-4e20-a66f-7c29f8e08705" />
<img width="757" height="558" alt="image" src="https://github.com/user-attachments/assets/2e4f4dd3-78a3-405e-91bd-e2a3fc0b2d8a" />



## 27) If update like open source project of Kubernetes has accepted some request of one of the user then definitely it will not reflect onto your local branch or the repo that you have forked in your machine or GitHub account because you have forked before the merging that code so for that what do you use?
<img width="370" height="98" alt="image" src="https://github.com/user-attachments/assets/81f23c43-9486-43f6-b15a-414ac7bdb53c" />

You can go to your GitHub account and do with UI or you can also do it with manual step.
<img width="975" height="87" alt="image" src="https://github.com/user-attachments/assets/81da19cc-2178-4ed3-9c4f-37ba7d5019c9" />

Now reset the main branch of your origin to the main branch of the upstream.
<img width="975" height="159" alt="image" src="https://github.com/user-attachments/assets/6ce0ff4a-3755-49ad-a633-e80e3e0118bf" />

You can also run `git pull upstream main` but there is a difference between these two commands.
<img width="975" height="722" alt="image" src="https://github.com/user-attachments/assets/451fb3d8-ab10-4671-93d2-8a9c26de0955" />

## 28) Difference between `git fetch` and `git pull`
<img width="975" height="297" alt="image" src="https://github.com/user-attachments/assets/a8caaced-b651-4c85-8047-42efffc55faa" />

## 29) Rebase command
If I have created one file “1” and then commit, again created file “2” and commit, again created file “3” and commit, again created file “4” and commit.

But now I want to merge that all four commits into the one commit then using `rebase -i` you can use it.
<img width="440" height="375" alt="image" src="https://github.com/user-attachments/assets/91f2b3ef-8f96-4e2f-aa21-bc795e2393aa" />
<img width="388" height="412" alt="image" src="https://github.com/user-attachments/assets/6b9e0814-6d4b-4816-934d-72e28482d7ca" />


I want to merge all these 4 commits into a single commit.
<img width="975" height="87" alt="image" src="https://github.com/user-attachments/assets/194f92db-12b6-40a9-b835-6371adaeb7cd" />
<img width="471" height="508" alt="image" src="https://github.com/user-attachments/assets/69f8146a-8d85-4ce8-918d-811847808035" />
  <img width="453" height="377" alt="image" src="https://github.com/user-attachments/assets/443ba43e-47ca-4087-898d-391401d61edc" />

Then change the pick here to squash and update the code like in the screenshot.  
Squash means about a squash commit merge into that pick commit.  
Means here it is three squash has been merged in first pick.

## 30) Merging conflicts
These conflict often happen when if one user has changed the code in line number 3 and another people have also changed the code in line number 3.  
At that time Git will ask you to help which changes should be done.

---
 
<img width="818" height="432" alt="image" src="https://github.com/user-attachments/assets/23481fbc-cc59-474f-9f51-c72ca0e94a25" />
<img width="865" height="529" alt="image" src="https://github.com/user-attachments/assets/ec9ae7ca-4c44-481a-bd93-7eb40672ab37" />
<img width="503" height="238" alt="image" src="https://github.com/user-attachments/assets/c1a105d5-92ed-4f90-ba0b-ec8c72cc0081" />
<img width="975" height="178" alt="image" src="https://github.com/user-attachments/assets/7a50861f-dae8-467d-8aaa-c7c650a24ca2" />




### Example of `git reset` vs `git revert`
<img width="441" height="410" alt="image" src="https://github.com/user-attachments/assets/7be4d1ca-9c20-4820-b912-366e1ec2e611" />
<img width="548" height="434" alt="image" src="https://github.com/user-attachments/assets/6ea7cdcb-2e04-4bdb-bc35-a31e422b8076" />
<img width="566" height="441" alt="image" src="https://github.com/user-attachments/assets/6aa00b11-cc18-4157-98f6-bc6c83a46e1e" />
<img width="975" height="324" alt="image" src="https://github.com/user-attachments/assets/21232bac-35cd-4a1a-ae34-ff5dede3eb56" />


---

### Chat link of ChatGPT Git & GitHub session  
🔗 https://chatgpt.com/share/6854f029-3ebc-8002-bbe6-2e0292d127ba

### Git cheatsheet screenshot
<img width="595" height="656" alt="image" src="https://github.com/user-attachments/assets/a3d4c591-00ba-438d-a12e-94495be7afd0" />
<img width="582" height="468" alt="image" src="https://github.com/user-attachments/assets/b3a0e067-c780-4aa5-bdd1-ddb0fec3d2f8" />
<img width="708" height="694" alt="image" src="https://github.com/user-attachments/assets/20f928d6-9b87-47fe-b11b-7e7706ef1b5b" />
<img width="717" height="294" alt="image" src="https://github.com/user-attachments/assets/ddac5bfe-944b-43cb-8abf-7ee47cc51a61" />
<img width="975" height="598" alt="image" src="https://github.com/user-attachments/assets/8116dbe0-eed1-4bb7-be67-c03e221c0086" />
<img width="618" height="183" alt="image" src="https://github.com/user-attachments/assets/34f761e1-35ed-4429-87c2-beda2b29367c" />

---

### Git commands reference  
🔗 https://github.com/Bhavya2520/DevOps-Learning/blob/main/docs/git/commands.md
