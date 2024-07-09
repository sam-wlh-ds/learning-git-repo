# Heading

This is a test to create

This is a test to update

## Sub Heading

This is a test done in Visual Studio

git clone <repo_name>

save changes

git add . (. for saving changes made throughout the repo)

if modified files (not newly created) [commit with add]
-> git commit -am "title" -m "description"

git status (check status of repo)

git commit -m "<title of commit>" -m "<description of commit>" (Saved code locally not on github)

git push
    if not ssh key generated:
        generate ssh key:- ssh-keygen -t rsa -b 4096 -C "<your_email>"
        -> Enter file in which to save the key : [Press Enter]
        -> Enter passphrase : <pass_phrase>
        -> Your identification has been saved in /home/<user>/.ssh/id_rsa
        -> Your public key has been saved in /home/<user>/.ssh/id_rsa.pub (Click on this and copy)
            -> Don't share private key (<file_name>) with anybody only share public key (<file_name>.pub)
        GO to setting in GitHub and add this to ssh keys
        Let your device know about your private key:
            eval "$(ssh-agent -s)"
            ssh -add ~/.ssh/id_rsa

DEFAULT location:
-> git push origin HEAD:main (new)
-> OR git push origin HEAD:master (old)
-> git push -u origin main (set deafault so next time you can only use git push)
Create-New-Repo:   
    git remote add origin <new_empty_repo_link>
    git remote -v (see the linked repo)
Braching:
    git branch
    git checkout -b <new_branch_name>
    git checkout <branch_name>
    git push -u origin <branch_name>
diff:
    (from main): git diff <branch_name> (exit: q)
pull:
    git pull -u origin master (get the lasted updated code)
merge:
    (from brach): git merge master
    -> fix conflicts 
delete (after merging with main):
    git branch -d <branch_name>
Undoing Git Commit:
    Last Commit:
        -> git reset HEAD~1 (HEAD~1 : pointer to the latest change)
    Other Commits:
        -> git log (see all your commits) [Get hash of the commit]
        -> git reset <commit_hash> (don't change the code just forget the commit)
        -> git reset --hard <commit_hash> (change the code as it was before the commit and forget the commit)

FORK: Forking a repo gives you full admin access to that repo as it copies that repo in to your account , you can change it as you want
but the changes will only be only in your account to make changes in the original repo you need to create a pull request (Do directly by GitHub).