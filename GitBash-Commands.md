### Command for making a new branch and using that branch
  * git branch branch_name or git checkout -b branch_name (b means git runs git branch branch_name then git checkout branch_name
  * git checkout branch_name
  * git add . or -A
  * git commit -a -m "Message"
      * -a for committing everthing
      * -m for adding the comment
  * git push -u -f origin branch_name
      * -u allows to use remote origin as default for easy push and pull without specifying origin again n again
      * -f allow to overwrite everything on directory
 
### Pushing project on Github
  * git init . 
  * git add -A
  * git commit -m "Message"
  * git remote add origin git@github.com:username/repo_name.git
  * git push -u -f origin branch_name
  
### Cloning a repo
 * git clone https_link copied from repo in the local repo from remote repo
 
 ### Checking the list of ssh keys
   * ls -al ~/.ssh
   * if ther files like id_rsa or id_rsa.pub then public and private key pair exists
   
 ### Generating SSH keys
  * ssh-keygen -t rsa -b 4096 -C "emaillinkedtoaccount"
  * then press enter
  * then enter the passphrase
  * start the sssh-agent
     * eval $(ssh-agent -s)
  * add the generated ssh key to ssh-agent
    * ssh-add ~/.ssh/id_rsa
  * remove the ssh key from ssh-agent
    * ssh-add -D ~/.ssh/id_rsa
    
  ### Adding SSh key to github account
    * clip < ~/.ssh/id_rsa.pub
      * copies the content of id_rsa.pub to clipboard
    * go to settings->SSh-> new ssh->add title and paste the file in description -> create  
      
  ###  Normal Commands
     * git status
     * git fetch -all + git merge = git pull
     * To remove something from remote repo: git rm -r --cached name_folder_or_file
     * git log for commits history, git log -n 2 , git log --oneline, git log --stat, git log -p (To get out of it use shift:)
     * git remote -v
     * git config --global user.name "github_username"
     * git config --global user.email "github_email"
     * git config --list
     * git checkout -- filename: discard theb uncommitted changes
     * git stash: The command   saves your local modifications away and reverts the working directory to match the HEAD commit.
     * git stash list: The modifications stashed away by this command can be listed 
     * git stash show: Inspected 
     * git stash apply: restored (potentially on top of a different commit) . Calling git stash without any arguments is equivalent to git stash push
     * git reset --hard
     * git stash list/apply/pop/save
     * git remote rm origin: To remove origin in .git file
     * git reset --hard: discard all the local changes in branch permanently
     * git rm -r --cached folder_name: to remove folder from git repo not locally mentioned in .gitignore after this do git commit and git push
     * touch .gitignore: to add .gitignore file to repo
     
