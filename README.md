# git_github
This repository serves as a comprehensive guide to understanding Git and GitHub, curated for learning purposes. It covers everything from the basics of version control to more advanced Git operations, making it ideal for beginners and intermediate users alike.
# Git & GitHub Notes

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
<img width="975" height="182" alt="image" src="https://github.com/user-attachments/assets/fafc4bd3-672d-4768-93cc-35a8e3d9981d" />
<img width="759" height="475" alt="image" src="https://github.com/user-attachments/assets/886bf727-fb8b-407e-8b10-34e1e53eb790" />


```

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

If you do not want to lose your current status of the git and also do not want that changes in your repo.  
You're just saying: just go back to the stage and when I need I will call for you.

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

## 22) If you have created a type of branch separately and add one feature on that and you want to merge that feature on the main branch then how can you do it?
For that you need to create PR request.

**Note:** If one branch is `<main>` and another branch is `<new feature>` then if `<new feature>` branch has made a request to push the code onto the main branch, only one time pull request has been created.  
And after that again if you commit some other things onto the `<new feature>` branch at that time new pull request is not being generated — it is automatically added into the main branch.

## 23) At a time only one PR is open

## 24) But I have confused in that if I feel like I have completed my feature and after the code reviewer says that you have to add these things and I have to add those things into my branch but I have already created one PR for pushing my code already with the main branch — so if I commit the new changes in my branch, that is also reflected on the main branch?

## 25) Merging main branch with my feature branch and after two months the client says that I want these changes in this feature so I have already created PR previously — I have just explained — then I need to change the code or change the new feature — then in that case what should be done

## 26)

## 27) If update like open source project of Kubernetes has accepted some request of one of the user then definitely it will not reflect onto your local branch or the repo that you have forked in your machine or GitHub account because you have forked before the merging that code so for that what do you use?
You can go to your GitHub account and do with UI or you can also do it with manual step.

Now reset the main branch of your origin to the main branch of the upstream.

You can also run `git pull upstream main` but there is a difference between these two commands.

## 28) Difference between `git fetch` and `git pull`

## 29) Rebase command
If I have created one file “1” and then commit, again created file “2” and commit, again created file “3” and commit, again created file “4” and commit.

But now I want to merge that all four commits into the one commit then using `rebase -i` you can use it.

I want to merge all these 4 commits into a single commit.

Then change the pick here to squash and update the code like in the screenshot.  
Squash means about a squash commit merge into that pick commit.  
Means here it is three squash has been merged in first pick.

## 30) Merging conflicts
These conflict often happen when if one user has changed the code in line number 3 and another people have also changed the code in line number 3.  
At that time Git will ask you to help which changes should be done.

---

### Example of `git reset` vs `git revert`

---

### Chat link of ChatGPT Git & GitHub session  
🔗 https://chatgpt.com/share/6854f029-3ebc-8002-bbe6-2e0292d127ba

### Git cheatsheet screenshot

---

### Git commands reference  
🔗 https://github.com/Bhavya2520/DevOps-Learning/blob/main/docs/git/commands.md
