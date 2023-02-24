mkdir lab02
cd lab02
git init
echo "Creating repo remotely" >> README.md
git add .
curl -u "Tocsaine" https://api.github.com/user/repos -d '{"name":"lab02"}'
git remote add origin https://github.com/Tocsaine/lab02.git
git commit -m "commit 1"
git push -u origin master

writting bad "Hello world!" program
git add Hello_world.cpp
git commit -m "comitting wrong hello world"
upgrading hello world...
git add -u Hello_world.cpp
git commit -m "Hello world with your name"
git push -u origin master
git log

git checkout -b "patch1"
changing hello_world.cpp
commit
git push origin patch1
creating pull-request
creating some comments in patch1's code
commit, push
self-checking
git checkout master
git merge origin/patch1
git push origin --delete patch1
git push origin master
git log
git branch -d patch1

git checkout -b "patch2"
clang-format -style=Mozilla -i Hello_world.cpp
commit, push, creating pull request.
git checkout master
creating some changes in comments...
commit, push master -> master
We are having some conflicts
git checkout patch2
git rebase master
git add Hello_world.cpp
git rebase --continue
git push --force origin patch2
Now there are no conflicts in PR
Merge patch2 -> master

