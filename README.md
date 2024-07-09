# Heading

This is a test to create

This is a test to update

## Sub Heading

This is a test done in Visual Studio

git clone <repo_name>

save changes

git add . (. for saving changes made throughout the repo)

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
-> git push origin master