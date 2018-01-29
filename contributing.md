# Submitting Code to a Pure Storage OpenConnect Project

1.	Make sure you have your own GitHub account. Create it here: https://github.com/join?source=header-home
2.	Find the project github page and fork a copy to your personal github account. Use the "fork" button, top right to do this.
3.	Get yourself a Linux node with a clean distribution, Ubuntu 16.04LTS is a good starting point and make sure it is up to date
4.	Install git on your node using yum/apt
5.	Check the developer documentation to see what toos are good for your development environment. For example, using Python install pylint using pip install pylint. I recommend running pylint against all your code before any commits as the Cis will fail the initial pylint tests if you haven't done your own due diligence
6.	Get the URL of your forked copy. On the website this is a button marked "Clone or download" near the top right of the page
7.	Clone your local repo fork of the project
```
git clone <URL of forked copy>
```
8.	cd into the directory just created to see your cloned source code
9.	Set the upstream location for your repo. You will need this to rebase your code later as changes to the master repo will need to be caught up on your branch at some point
```
git remote add upstream https://github.com/ansible/ansible.git
```
10.	Now create a branch of the code 
git checkout -b <some appropriate name>
11.	Always remember to code in your own branch. Never in the master branch!! Bad practice and you won't be able to commit changes that way as you won't have permission anyway.
12.	You are now ready to do your coding - work your magic!!
13.	When you are ready to submit your code you need to commit your changes to your personal repo. First add all your changes then commit
```
git add <new or modified files>
git commit -a 
```
14.	Ensure your branch is up to date on your personal fork: git push origin HEAD
15.	You now have your new code in a branch on your personal repo
16.	Now you have to issue a Pull Request (PR) on the main development branch of the project. Do this from within the github website on your repo page. Look for a button called "Compare & pull request" that should have appeared on your github webpage. Select the master delevopment branch in the project repo and your newly committed branch in your local repo.
17.	You will see your PR on the main project website. This will probably have some CI tests run automatically. Look at the PR to check the results of these CI tests. Don't be surprised if they fail initially - your code will probably need some tweaking to make the CI succeed. The developers website with instructions is probably out of data or missing stuff you need.
18.	Now go fix your code, making sure you are in your development branch. Check this with git branch . You are in the branch with the asterix. If you need to change branches use git checkout <branch>
19.	When you have performed the fixes, push the changes to your local repo branch again
```
git add <changed files>
git commit -a -amend origin/<branch name>
```
20.	If a long time has passed between your initial clone of the master repo and your code submissions the commit may fail and your will be forced to rebase your code. Do this using the following command:
```
git pull --rebase upstream <master devel branch>
```
Now you can try your commit again.

21.	Ensure your branch is up to date on your personal fork: git push origin HEAD
22.	This will automatically update the PR and kick off the CI tests again 
23.	When you have the CI tests passing now yo have to wait for/encourage the moderators to check/comment/approve your code changes. When everyone is happy your changed will be merged.

