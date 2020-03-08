# cuddly-lamp
GIT DEMO
-------------------------------------
git clone 
cd 
[master]
git add 
git commit 
git push
git pull
--
git branch [develop]
git checkout develop
git commit -am
git push --set-upstream origin master
git commit -am
git push origin
--
git checkout -b feature/new-feature
git add -A
git commit -m 
git push --set-upsteam origin feature/new-feature
-- 
pull request and merged 
--
git checkout develop
git pull origin
git remote -v
--
git checkout master
git checkout master  --> your branch is behind 'origin/master' by 5 commits.
git checkout develop --> your branch is up to date with 'origin/develop'.
git checkout feature/new-feature --> your branch is up to date with origin/feature/new-feature'
git branch -vv
--
git checkout master
git fetch
git merge
--
what is github's pull request ==> once changes are committed and pushed to 'feature' branch, it needs to be merged into 'develop' beanch. therefore inorder to merge them we create 'pull request'.
--
created a branch directly on Github and merged into develop
git checkout develop
git pull origin
-----------------------------------
Assignment:
create 2 feature branches from develop 
checkout to them, add files then commit and push 
merge them with origin/develop 
lastly merge develop into the master.
-----------------------------------
step 1:
	git branch feature/search-feature
	git branch feature/login-feature <br>
step 2.a:
	git checkout feature/search-feature
	[file-saved]
	git add -A
	git commit -m "Adding search file"
	git push --set-upstream origin feature/search-feature
step 2.b:
	git checkout feature/login-feature
	git branch --set-upstream-to=origin/develop feature/login-feature 		**mistake
	git pull origin
	git branch --set-upstream-to=origin/feature/login-feature feature/login-feature ==> **error: the requested upstream branch 'origin/feature/login-feature' does not exist
	git push origin HEAD					**resolved mistake, here only branch name pushed so I set it as origin in next step
	git branch --set-upstream-to=origin/feature/login-feature feature/login-feature
	[file-saved]
	git add -A
	git commit -m "initial login commit"
	git push origin
step 3: 
	[Github]branch: develop, 	base: develop <-- compare: feature/login-feature
	git checkout develop
	git pull origin
step 4:
	[Github]branch: master, 	base: master  <-- compare: develop,		Create Pull Request, 	Merge pull request
	git checkout master
	git pull origin

