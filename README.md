# devops_edu

How to install git and some basic commands
#
    sudo apt update
    sudo apt install git -y
To check the installed version
#
    git --version
To get help or see what are all cmd
#
    git help
To list branches
#
    git branch
git command used to start a working area
#
    git init
You may view additional help on each command following the syntax git help <command>. For this you must first install git man pages using the command
#
    git help init

Once a git repo is intializes we can see some of the hidden files ls -a ( like .git ) unit we create some file it cannot show anything on git status cmd
we have 3 stage(working area ) (staging area) (commited files)

 <img width="967" alt="Screenshot 2024-10-06 at 8 41 44 PM" src="https://github.com/user-attachments/assets/6199f2b5-7bb1-4aa4-9c83-def79666fdf2">

To create an empty file  and wirite some text to the file
 #
         touch story1.txt
         echo "my  frist line1"
        

To view the status where we are now on those there stage we can use git status cmd
#
        git status
        git ls-files

To add the file to the staging area 
#
        git add story1.txt
        git status
        git ls-files

To commit the file 
#
        git commit -m "added frist story"

        git status
        On branch master
        nothing to commit, working tree clean

Now once we make changes to the story1.txt we can see the file is being tracked but in modified state.

       <img width="517" alt="Screenshot 2024-10-06 at 8 54 33 PM" src="https://github.com/user-attachments/assets/e110ebe4-6c9a-471e-b2e5-b64c71855a46">

       we can use a git cmd to restore as well
#
        git restore story1.txt

Now the file is back to orginal postion and its clean git status
But lets add 2ine and add and commit

#
        echo "secondline" >>stroy1.txt
        git add story1.txt
        git commit -m "updated friststory"


Now lets add second file we can see the untracked file modified file staging area 

 <img width="522" alt="Screenshot 2024-10-06 at 9 02 17 PM" src="https://github.com/user-attachments/assets/38f728fd-b34a-4b15-8bfa-773ee25422f2">

 #
         echo "line1insecondfile" > story2.txt
         git status
         git add .
         git commit "added story2.txt"


Playing to move file from working area to staging area and staging area to working area

<img width="376" alt="Screenshot 2024-10-06 at 9 10 46 PM" src="https://github.com/user-attachments/assets/6de3cfb8-932d-47e9-bf6a-a30245be2d84">

#
        echo "thirdline" >> story1.txt
        git add story1.txt
        echo "line2insecondfile >>story2.txt
        git status

        git restore --staged story1.txt

        git add story2.txt
        git commit -m "updating story2.txt"

git log is the command to see the commit id date of the commit happened and commit message
#
        git log

we can list the changed files as well using the --name-only
#
        git log --name-only
we can see online of commit log
#
        git log --oneline
To view only last 2 logs we can change the number 2 to 3 4 depending on the logs required.
#
         git log -n 2

Branching in git

<img width="798" alt="Screenshot 2024-10-07 at 5 21 14 PM" src="https://github.com/user-attachments/assets/f2ab67d4-b3a9-4b2d-873f-54946c91358d">

#
        git branch newfeature
        git checkout newfeature

        or it can be done in single cmd
        
        git checkout -b newfeature

        not make some changes to the story1.txt

        git add .

        git commit -m "updated branch"

        not make some changes again to the story1.txt

        git add .

        git commit -m "updated branch secondtime"

        git checkout master

        git merge newfeature

        git log

        git branch -d newfeature

        git branch  ## to see the branch doesn't exist
        










        



