# Git Commands
git config					#Configure the username and email address

git init  					#Initialize a Local Git Repository

git init --bare				#No .git subfolder. Does not contain any source files

git add . 					#Add one or more files to staging area

git commit -m "Message" 	#Commit Changes to head

git status					#Displays the state of the Working directory and staging area

git diff 					#View the changes made to the File

git log

git log --pretty=online

git add remote origin Server_Repo_URL

git push -u origin master

git clone Server_Repo_URL

git reset --soft 			#Undo local changes to the state of Git repo

git revert Commit_ID

#Git Branch Commands

git branch New_Branch

git push -u origin New_Branch	#Upload contect from local respository to a remote respository

git branch -av

git merge New_Branch		#Merge a branch into an active branch

git branch -D New_Branch

git push origin -delete New_Branch

git pull					#Fetch and download content from a remote repository

git mv						#Rename a file

git stash 					#Allows you to switch to another branch to work on something else

git diff-tree -r {commit hash} 		#List of files that has changed is a particular commit
# -r allows the command to list individual files
# commit hash will list all the files that were changed or added in that commit

# Only downloads new data from a remote repository
git fetch origin 
git fetch --all

# Updates the current head branch with the latest changes from the remote server
git pull origin master

# Git Config
git config --global user.username <github username>
git config --global user.username  "amb"
git config --global user.email ' amb@gmail.com'
OR
git config --global user.name  "amb"
git config --global user.email  amb@gmail.com

git config --list

# Resolve Merge Conflict
git log --merge 			    #List of commits that are causing conflict
  
git diff					        #Finding differences between the states of repo
  
git checkout			    	  #Undo changes made to the file, or for changing branches. 
  
git reset --mixed 			  #Undo Changes to the working directory and staging area
  
git merge --abort			    #Exiting merge process and returning back to the state before the merging began
  
git reset					        #Used at the time merge conflict to reset the conflicted files to their original state
  
git pull --rebase origin <branchname>
  
git mergetool
  
git rebase --continue
  
git log -n 2


# Git Instructions Step-by-Step
mkdir git_dir
mkdir /git_dir/MyRepo
git init
touch master.txt
git status
git add .
git commit -m "Commiting my first Repo"
git status
git log

# Login to Github
New - Repo - Repo Name (MyRepo)- Description - Private/Public - Create Repo

# - To Push a file from your local system onto Github
# - First, connect to the local repository to your remote repository:
git remote add origin <copied web address>
git remote -v
# - Second, push your file to the remote repository:
git push -u origin master

# SSH-KEY
Your Profile -settings - ssh and GPG keys - New SSkey
ssh -T git@github.com
Go to Github - New create new repo
Initialize read me
git clone (ssh url)
git push -u origin master

# Create Branch
git branch <branchname>
git branch -v

# Check Out Branch
git checkout <branchname>

# Delete Branch
git branch -D <branchname>
git push -u origin -d remote_branch_name
git branch -d  local_branch_name



