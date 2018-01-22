# Add-Code-to-GitLab

Check if Git has already been installed 
Git is usually preinstalled on Mac and Linux.

Type the following command and then press enter:

git --version
You should receive a message that will tell you which Git version you have on your computer. If you don’t receive a "Git version" message, it means that you need to download Git.

If Git doesn't automatically download, there's an option on the website to download manually. Then follow the steps on the installation window.

After you are finished installing, open a new shell and type "git --version" again to verify that it was correctly installed.

Add your Git username and set your email 
It is important to configure your Git username and email address as every Git commit will use this information to identify you as the author.

On your shell, type the following command to add your username:

git config --global user.name "YOUR_USERNAME"
Then verify that you have the correct username:

git config --global user.name
To set your email address, type the following command:

git config --global user.email "your_email_address@example.com"
To verify that you entered your email correctly, type:

git config --global user.email
You'll need to do this only once as you are using the --global option. It tells Git to always use this information for anything you do on that system. If you want to override this with a different username or email address for specific projects, you can run the command without the --global option when you’re in that project.

Check your information 
To view the information that you entered, type:

git config --global --list
Basic Git commands 
Go to the master branch to pull the latest changes from there 
git checkout master
Download the latest changes in the project 
This is for you to work on an up-to-date copy (it is important to do every time you work on a project), while you setup tracking branches.

git pull REMOTE NAME-OF-BRANCH -u
(REMOTE: origin) (NAME-OF-BRANCH: could be "master" or an existing branch)

Create a branch 
Spaces won't be recognized, so you will need to use a hyphen or underscore.

git checkout -b NAME-OF-BRANCH
Work on a branch that has already been created 
git checkout NAME-OF-BRANCH
View the changes you've made 
It's important to be aware of what's happening and what's the status of your changes.

git status
Add changes to commit 
You'll see your changes in red when you type "git status".

git add CHANGES IN RED
git commit -m "DESCRIBE THE INTENTION OF THE COMMIT"
Send changes to gitlab.com 
git push REMOTE NAME-OF-BRANCH
Delete all changes in the Git repository, but leave unstaged things 
git checkout .
Delete all changes in the Git repository, including untracked files 
git clean -f
Merge created branch with master branch 
You need to be in the created branch.

git checkout NAME-OF-BRANCH
git merge master
Merge master branch with created branch 
You need to be in the master branch.

git checkout master
git merge NAME-OF-BRANCH



https://docs.gitlab.com/ce/gitlab-basics/start-using-git.html

https://stackoverflow.com/questions/32125514/how-to-create-and-commit-a-branch-in-gitlab

https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add
