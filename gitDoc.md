Git Concept:
Local = Working Directory -> Stage -> Local Repository -> Remote
ShortCut terminal keyboard = cntr + shift + `

# Installation, init, status & clone

Create working Directory:
=>mkdir gitone (filname) </br>
To go forward from the current
=>cd gitone </br>
Inside gitone folder create file:
=>touch one.txt </br>
To get back working directory or back:
=>cd .. </br>
To initialize empty git repository
=> git init </br>
for clone file from Remote 
=>git clone https://github.com/jafrul55/gitfundamentallearn.git (link) </br>
To check all folder and file in current directory
=>ls </br>
To check status of file changes:
=>git status </br>

# git add and reset (stage):

To stage all file:
=>git add --all or git add -A </br>
To go stage to local (reset):
=>git reset </br>
To check folder (where we are)
=>pwd </br>
But If you want to commit in current file and folder:
=>git add . </br>
If you want to bring in stage all file and folder instead of deleted then you can use:
=>git add * </br>

You can bring in stage for specific file
=> git add filename.txt or git add foldername/filename.txt </br>
If you want to bring all .txt file in stage:
=> git add *.txt </br>

Local = Working Directory -> Stage -> Local Repository -> Remote </br>

Working Directory -> Stage [Stage] -> Local Repository -> Remote </br>
Stage -> Local Repository[Commit] -> Remote </br>

=>If I write git add . then all file will stage </br>

Now you can commit all stage file:
=> git commit -m "Your message" </br>
Now if you want to go back to the local again from commit then: [~tail symbol] </br>
=> git reset HEAD~ </br>
If you want to get back all changes file and deleted file in hard core:
=> git reset --hard </br>

# Git Remove

If you want to remove specific file and also stage it imediately then: (both will be happen)
=> git rm two.txt </br>
But If you change inside file content and want to remove it then it won't delete:
=> git rm two.txt </br>
But If you are stuborn to delete change file forcefully the:
=> git rm two.txt --f </br>
But If you want to delete change file in stage but you are not interested to remove from working directory then:
=>git rm --cached two.txt </br>
If you want to delete folder recursively:(folder in folder)
git rm -r foldername </br>

# Checkout, Brancing & Merging

To check git branch and how much branch available:
=>git branch [here * main mean we are in main branch] </br>

To create new branch in our branch:
=>git branch development(branch name) </br>
To switched development branch from main branch:
=>git checkout development </br>

If I change any file in any branch and the if we shifted to other branch then changes not be found because of branch.Different branch we can work different file. </br>
Ultimately you have to merging both after changes all branch files.
For merging development with main:
=>git merge main -m"message what you like" </br>
[main file all will come to development branch]

You can also merge development with main:
=>git merge development -m"message you like" </br>

Git merge conflict:
If development branch change file value and staging branch change file value become change the it will be comfusion to merge. 

<!-- $ git merge staging -m"merge try to done"
Auto-merging two.txt
CONFLICT (content): Merge conflict in two.txt
Automatic merge failed; fix conflicts and then commit the result. -->

for solve it any of them from the branch may be development or staging can take action to resolve it.
After taking action between to branch any of them can merge it.
After complete it you can merge with main branch.

# Git Push, Fetch & Pull

Local = Working Directory -> Stage -> Local Repository -> Remote
If I want to send Local Repository to Remote then we can use it by the push method.</br>

On the other hand:
If we bring Remote file into Local Repository then we can called it fetch.

Local Repository -> Remote = Push
Remote -> Local Repository (all changes) = fetch
Remote -> Local Repository (all file) bring back = Pull

TO send main branch all file in remote:
=>git push origin main </br>

You can do it for staging branch
=>git push origin staging </br>

You can do it for development branch
=>git push origin development </br>

Now we talk about fetch:
If I edit github/remote repository file and commit it remotely.
Now If I want to bring it back to the local repository from remote:
=>git fetch </br>
But fetch file you can not see. SO to see fetch file you also merge it
=> git merge </br>

You can use git pull (to fetch data and merge data) in the same time: [all file]
=>git pull </br>
