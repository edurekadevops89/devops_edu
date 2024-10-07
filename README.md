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

To add the file to the staging area 
#
        git add story1.txt

To commit the file 
#
        git commit -m "my1st commit"


        



