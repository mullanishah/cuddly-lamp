# cuddly-lamp
GIT DEMO
-------------------------------------
git clone <br>
cd <br>
[master]<br>
git add <br>
git commit <br>
git push<br>
git pull<br>
<br>
git branch [develop]<br>
git checkout develop<br>
git commit -am<br>
git push --set-upstream origin master<br>
git commit -am<br>
git push origin<br>
<br>
git checkout -b feature/new-feature<br>
git add -A<br>
git commit -m <br>
git push --set-upsteam origin feature/new-feature<br>
 <br>
pull request and merged <br>
<br>
git checkout develop<br>
git pull origin<br>
git remote -v<br>
<br>
git checkout master<br>
git checkout master  --> your branch is behind 'origin/master' by 5 commits.<br>
git checkout develop --> your branch is up to date with 'origin/develop'.<br>
git checkout feature/new-feature --> your branch is up to date with origin/feature/new-feature'<br>
git branch -vv <br>
<br>
git checkout master<br>
git fetch<br>
git merge<br>
<br>
what is github's pull request ==> once changes are committed and pushed to 'feature' branch, it needs to be merged into 'develop' beanch. therefore inorder to merge them we create 'pull request'.<br>
<br>
created a branch directly on Github and merged into develop<br>
git checkout develop<br>
git pull origin<br>
<br>
-----------------------------------<br>
Assignment:<br>
create 2 feature branches from develop <br>
checkout to them, add files then commit and push <br>
merge them with origin/develop <br>
lastly merge develop into the master.<br>
<br>
-----------------------------------<br>
step 1: <br>
	git branch feature/search-feature <br>
	git branch feature/login-feature <br>
step 2.a: <br>
	git checkout feature/search-feature <br>
	[file-saved] <br>
	git add -A <br>
	git commit -m "Adding search file"<br>
	git push --set-upstream origin feature/search-feature<br>
step 2.b:<br>
	git checkout feature/login-feature<br>
	git branch --set-upstream-to=origin/develop feature/login-feature 		**mistake <br>
	git pull origin <br>
	git branch --set-upstream-to=origin/feature/login-feature feature/login-feature ==> **error: the requested upstream branch 'origin/feature/login-feature' does not exist<br>
	git push origin HEAD					**resolved mistake, here only branch name pushed so I set it as origin in next step<br>
	git branch --set-upstream-to=origin/feature/login-feature feature/login-feature<br>
	[file-saved]<br>
	git add -A<br>
	git commit -m "initial login commit"<br>
	git push origin<br>
step 3: <br>
	[Github]branch: develop, 	base: develop <-- compare: feature/login-feature<br>
	git checkout develop<br>
	git pull origin<br>
step 4:<br>
	[Github]branch: master, 	base: master  <-- compare: develop,		Create Pull Request, 	Merge pull request<br>
	git checkout master<br>
	git pull origin<br>
<br>
