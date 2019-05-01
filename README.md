# gitsetup-commands
## git bash set up
1. Go to https://git-scm.com/downloads and download git bash set up for your respective OS.
2. Install exe file.
3. Once installed, go to one of your drive and right click, you must see an option "git bash here". Click this option.
4. Now its time to generate ssh key
 4.1 Enter ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
 4.2 Keep Entering till it generate your ssh private key and public key and notice that path where your files exists.
 Reference : https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key
5. Go to that drive say /c/Users/my user name/.ssh/ir_rsa.pub
6. Open the PUB file and copy the key inside it.
7. Paste this key in your git hub/bitbucket account's setting ssh key -> add option.

Now , you should be good with your git bash set up and ssh authentication.

## tortoiseGit set up
1. Download the corresponding set up for your OS from https://tortoisegit.org/download/.
2. Install the exe set up.
3. Once installed, right click on your drive and click "TortoiseGit" -> "Setting" ->Click on Network
4. Check your ssh client path. By default it points to tortoise.exe path and thus stops you from cloning your branch through tortoisegit.
5. Provide the correct ssh.exe path say "C:\Users\<your username>\AppData\Local\Programs\Git\usr\bin\ssh.exe"
6. Also check in general git.exe path is correct.
7. Click apply and Ok.

We should be good with git clone and using windows shell interface to git.

#### Useful command for CLI
1. git clone <your master/develop branch ssh/http url ex: git@github.com:er-kpawan/gitsetup-commands.git>
To clone your remote master branch to your local system


2. git checkout feature/your-local-branch
To switch to your branch


3. git branch 
To check which branch is your local branch currently pointing

4. git status
To check your local modifications

5. git add . or git add <file1 path> <file2 path>..
  To add files which are to be commited. git add . will add all files.
  
6. git commit -m "your message"
  To commit the added files in your local branch
  
 7. git push
   To send the committed files to remote server
   
 8. git push --force origin 42cbda16b59:feature/anybranch
   This will revert to certain commit say 42cbda16b59
   
 9. git revert 42cbda16b59(commit number) and then git push
 To revert to a commit.
 
 10. git branch <name_of_your_new_branch>
  To create a branch in local and if we want to push this to remote server then 
   10.1 git push origin <name_of_your_new_branch>
   
  11. git push origin :<name_of_your_branch>
   To delete a branch
  
 12. git checkout -b <your_new_branch_name> <your_origin_branch>
 To create a branch from another branch and points to the newly created branch
  12.1  git push origin <your_new_branch_name>
  To push your new branch to remote server
  
  13. git branch -D [name_of_your_new_branch]
    To forcefully delete your local branch
    
    
   
-------------------------------------------------------
## Updating local branch with master/develop branch
 If you are pointing to your local branch
 
 1. git pull origin develop/master
 2. git push
 
 
