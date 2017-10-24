# GitHub Tutorial

_by Xiurong Yu_

---
## Git vs. GitHub
Git: Keep **“snapshots”** of code & **does not require github**  
Github: **Stores code** in the cloud, visually track changes, & **requires git**.


---
## Initial Setup
**- Make a github account.**  
1. Go to [www.github.com](www.github.com)  
2. Click sign up in the upper right hand corner.  
3. Step 1 will ask you to fill in a username, email address, and password you want to use.  
<img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/4b6ae1fec8c51ff9bf9e7752847116c29710237c/create%20account%20step1.PNG" id="c9.io" alt="" /> 
4. Step 2 will ask you to choose a plan.
    * Usually you would choose free plan unless you wan to use the other one.
5. Step 3 will ask you some question and you will answer them.
6. Click submit once you completed all steps.
7. Go to the email address you out down when signing up to github.
    * You should see a message from github that askes you to verify your email address. 
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/08fe27f74d4bb7d5fc5dd763ceef793333311ec6/vertify%20email%20address.PNG" id="c9.io" alt="" /> 
    * Click on Verify email address and it will bring you to your github account. This means your email address is verified and you are able to access github features!


**- SSH setup**
1. Click on profile icon on the upper right hand corner and press settings.   
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/b178b73bd44301eff2e600d907b34c35a88fc029/sshkey1.PNG" id="c9.io" alt="" />  
2. Then on the leftside bar (under personal setting), click on SSH and GPG Keys.
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/eec3e139b82de6ece3514282e19eccbc3ee7bd3b/sshkey2.PNG" id="c9.io" alt="" />  
3. Click New SSH key
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/f7275c5a9ab414292b372bb1a994384c58c99ecc/sshkey3.PNG" id="c9.io" alt="" />  
4. Go to your cloud9 account. Click on the gear icon on the upper right.
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/7838be5290ae2ba4ba68e8f724463db496095d55/gear%20icon.PNG" id="c9.io" alt="" />  
5. Click on "SSH Keys" on the left.  
6. Copy the 2nd SSH Key to your github account.
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/5a0875db3b44d192dc8af6d37a1543017a117b0b/sshkey4.PNG" id="c9.io" alt="" />  
7. Your SSH is now set up!


---
## Repository Setup
**- Making a Repository (repo) and initialize git**
1. Go to your github account that you have created. On the upper right hand corner, click the "+" sign and create a new respository.  
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/8f648e44f52da650741f26163ba486b0cb25b7db/make%20repo.PNG" id="c9.io" alt="" /> 
2. Give your repository a name (In this case I named it tutorial-repo). Once your repository is created, you should be seeing this     <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/f192d3392b30669d574da82586be6f30ebcf1840/reposetup_.png" id="c9.io" alt="" /> 
3. Copy the SSH link on github
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/8e064dd66c792342c43c3a38f5f8740e2f06c739/sshlink.PNG" id="c9.io" alt="" /> 
4. Go to your cloud9 account. On a new terminal/workspace and type in the following and paste the link after git clone.
`git clone [link]`  
5. Everytime you clone something, **always cd into it**  
`cd [name of the repo]`  
6. Make a file in this repo and name it README.md (this will help you practice git add & git commit later on)
`touch README.md`  
7. Now initialize git inorder to use git commands
`git init`
* You should be seeing something like this
<img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/71b7da663b83e9e44b9eae86579a6d025895b034/gitinit.PNG" id="c9.io" alt="" />  
    * Note: Do not ever git init in workspace because it is a empty git repository.  
    * However, if you already initialize it  
    `rm -rf .git` will help you remove it  
    * Notice the (master) is gone when you uninitialize git
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/c70ad3ef640ebabb00cdb923ebc9ae857ef7df62/remove.git.PNG" id="c9.io" alt="" />

**- First add and commit**
1. Go to the readme file you creaded in cloud9 (the one you cloned from github)  
`cd [your repo]`

2. Open up the README.md file you created inside this folder and type in any message you want.
 <img src="https://raw.githubusercontent.com/xiurongy3506/first-repo/81bff2422a0930d773b7f0aaf6999b23b8c156f3/readme.PNG" id="c9.io" alt="" />  

3. Now go back to the command line, and add this file to staging area.  
`git add README.md"`

4. Once you have added the file, commit it with a message that will help you reference what you did.
`git commit -m "[message]"`  

5. Now you have to set connection with your remote repo in github in order to push your commits. Use the following format  
`git remote add origin [URL]  `  

* Once you added the remote origin, you no longer have to added next time unless you want the file to go to a diferent remote.  
   * you can find the URL under "...push an existing repository from the command line"
    <img src="https://raw.githubusercontent.com/xiurongy3506/github-tutorial/f192d3392b30669d574da82586be6f30ebcf1840/reposetup_.png" id="c9.io" alt="" />

6. Now type the second line of the code  
`git push -u origin master`
* This is only for the first time set-up; this means the next time you can just use `git push`to push into the same repo in github.
    * You should be seeing the following after you push showing that you have successfully pushed your README file on github  
    <img src="https://raw.githubusercontent.com/xiurongy3506/first-repo/master/gitpushresult.PNG" id="c9.io" alt="" />  

7. Go back to your github account, open your repo, then pressed commits.  
    * You should be able to see the commit you pushed (For your repo, you should only see one commit)
     <img src="https://raw.githubusercontent.com/xiurongy3506/tutorial-repo/3bae62b6dfda58f1b11049f4c05ea1df497b095a/commits.PNG" id="c9.io" alt="" /> 
---
## Workflow & Commands
If you want to commit another file to github(the remote repository), the process will be different. Let's commit another mesaage to the same README.md file we've been working on.  
1. Make sure you are on your repo in a command line (at cloud9)
* You should see USERNAME: ~/workspace/[name of your repo] $  
2. Open up your README.md. You can use the following to help you open.
    * c9 README.md  
3. Add or delete anything in the text go back to your terminal.  
4. Now add your file to the staging area  
`git add README.md`  
5. Use `git status` to check the state of your file
* You should see README.md in green showiing that it can be commited
 <img src="https://raw.githubusercontent.com/xiurongy3506/tutorial-repo/f7b6bc5b05271d0e818b655f059dc4af96599ee0/commit.PNG" id="c9.io" alt="" />  
6. Now commit the file by stating what you did to the file
`git commit -m "[text]"  
7. Push the commit to the remote. This time you don't have to do `git remote add origin [URL]`or `git push -u origin master` because it is a one time set-up that is already added. So just simply type
`git push`
* You should still see something similar to 
 <img src="https://raw.githubusercontent.com/xiurongy3506/first-repo/master/gitpushresult.PNG" id="c9.io" alt="" />  
8. Now you can go to github and check the commits in your repo. 
* You should see another commit being added.

---
## Rolling Back Changes
undo edit/add/commit/push
**- Undo edit**
1. Make sure you are in USERNAME:~/workspace/[name of repo]. If not cd into it.
2. Go to your README.md and add some text.
3. Now use git status to check the stage of your file (try to use this command frequently to check your state of file)`git status`
4. Now notice the nessage above the README.md is red because you have not added to the staging area. Also, there are command listed for how to discard a change.
5. Type in this command without using <> or ....
`git checkout -- [file]`
 <img src="https://raw.githubusercontent.com/xiurongy3506/tutorial-repo/7c98343c551fa4856e2a8de206a7aaf2d4a3b03f/undoedit.PNG" id="c9.io" alt="" /> 
6. Now go open up your README.md  
`c9 README.md`
7. You should see the texts you added being deleted.

**- Undo add**
1. Make sure you are in USERNAME:~/workspace/[name of repo]. If not cd into it.
2. Make some changes to your README.md.
3. On the terminal, add your README.md to the staging area.
`git add README.md`
4. Your README.md should be showing up as green because it is being added to the staging area.
5. Now Check the state of your files
`git status`
 <img src="https://raw.githubusercontent.com/xiurongy3506/tutorial-repo/17ce9e33dc665f7abeb33db5d6122c4d65bee426/Capture1.PNG" id="c9.io" alt="" /> 
6. Since your README.md is green, you want to unstage it (turn it to red) using the command given above
`git reset HEAD README.md`
7. Now use `git status`, and you should be seeing your README.md unstaged (red).

**- Undo commit**
1. Following from the step above, add README.md to the staging area.
`git add README.md`
2. Your README.md should appear green. Now commit it with a message.
`git commit -m "[text]"
3. You have just commited README.md, but you want to undo it. Use the following to help you undo the commit.  
`git reset --soft HEAD~1`
4. You have just undo your commit!

**- Undo Push**
1. Make sure you are in USERNAME:~/workspace/[name of repo]. If not cd into it.
2. Add some text to README.md
3. Add and commit it
4. Then `git push`. This will allow you to see your commits in the remote repo.
5. At this point, you realized that you did not mean to push it and you want to undo your push. Use the following to undo a push.
` git reset --hard HEAD~1`












