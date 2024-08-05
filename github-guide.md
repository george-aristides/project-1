# Please read before working - github version control for this project

I know this is a lot of stuff you already know how to do, but to be thorough I am going to document every step 
If you have questions or are confused about anything related to the github process PLEASE make sure to refer to this, look it up, or better yet ask someone for help! 
Making mistakes with this can sometimes cause really annoying problems for yourself or other collaborators, which is something I have done to myself on solo projects, and fixing them can be a pain.

I have worked on projects/teams with a lot going on so I am doing my best to use what I learned from those experiences in this guide. If you notice any mistakes or have suggestions or anything else please let me know. I am doing this from memory plus I may just be wrong sometimes so feedback is appreciated.

To do work on this, start by cloning the repository.
Open terminal and go to the place you want to store your local copy of the repo
For me, I like to keep them on my desktop, so I will type "cd/Desktop" to go there

Once you are where you want to be, make sure you click the green Code button on the main github page for the repo to get the http or ssh link (whatever you prefer) and copy that
You can then go back the terminal and type 'git clone <link here>' where you paste the link in 
If you use ssh you will have to enter your ssh password, if you don't know what this is don't worry about it. It doesn't really matter for this project 

Now that you have cloned the repository successfully, make sure you open it in your terminal with "cd/project-1" - assuming you are already in the place it is stored
In my case, since I keep them on my desktop I need to go to "cd/Desktop/project-1" every time I open a new terminal session

# Branches
I have created a second branch, called "dev" - which means development. This branch is separate from "main" and it is best to keep it this way.
The reason for this is so we can put things that we think are functional and finalized into dev and have that be a second branch to work on with things that are not ready to be incorporated into the main branch
This is good because we can prevent things like mistakes or conflicting changes/files from being pushed into the main code.
Basically, if we are all just pushing everything into the main branch, we could overlap, overwrite, or put things that don't work properly in and it would make it difficult to work together and recovering the older version becomes more difficult than it needs to be
It is like all of us trying to type the same essay on the same document at the same time in a google doc, it gets messy, you write in the middle of or over other peoples stuff, delete the wrong thing... you get the picture

We may decide to change how we do our branch system, but this way is pretty standard so I set it up this way initially

To open an existing branch, please make sure you are in the local respository in terminal, and type "git checkout <branch name>"
So, to open dev, "git checkout dev"
If you want to know what branch you are on at any point, type "git status" and it will tell you

*please do not create a new branch called dev or main, or with the same name as any other existing branch* 
To create a new branch, type "git checkout -b <new branch name>"
This command will create a new branch locally (meaning on your device only) and switch to it. You will then have to commit those changes (creating a new branch is a change) to the online repository for other people to see your branch
Depends on what we decide to do, but generally don't just create branches for no reason. It makes things messy.
You will want to create a new branch for each change you plan on making, I think we can/will discuss this in greater detail.


# Upstream
So far we have cloned the repository to your local machine and switched to the dev branch

When you clone the repository, you pull down the existing code, but the default branch for changes is "main"
In order to set up other branches to be "upstream" - which means that you can push changes within that branch up the online repo - you need establish on your device that it is an upstream branch

To do this make you are in the right branch, so you can go "git status" to see. If you are not in the right branch (which for now is "dev") you can to "git checkout dev" to switch to it
Once you are in the branch you want to set as upstream, you can type into terminal "git branch --set-upstream-to=origin/dev" and replace dev with the other branch name if needed 
To make sure this worked, you can type "git branch -vv" and it will show you the status of each branch - it should say [origin/dev] if it is upstream
This means you can now type commands like "git push" and "git pull" directly from your branch without having to specify anything else

# Push and Pull
In order to make changes or update your local repo, you can push and pull
If you make changes - lets say you create a new file on the dev branch on your local machine and edit another existing file locally (since every change you make on your computer will be local)
this is how you can handle moving those changes to the online repo

## Push
the first thing you can do - and especially in the beginning its really good to do this between EVERY step to get a feel for whats happening and make sure you don't make silly mistakes - is type "git status"
This will show you any differences between your local repo and the one on github, so you will see what files have been created, deleted, or altered

Checking the status of course does not move the changes, so the first step in moving changes is "git add"
You can't move your changes to the online repo without doing these steps, for good reason
"git add" adds our file to the staging area, to stage them for a commit

You have to specify the files you want to commit, so just saying "git add" won't do anything and will give an error message
It should look like this "git add <file1> <file2> ..." where <file1> and <file2> are the names of files and you can keep listing them
Alternatively, if you want to add every change you have made from where you are to the stage, you can say "git add ." where the period "." means all, so it adds everything
This is not considered good practice, but for this project I would imagine it should not be a huge deal and I can not lie to you and say I won't probably be doing that 99% of the time
Just please make sure you are keeping track of all changes if you do this, if you have only one change or know all of your changes should go up, then its not a problem, 
but if you are messing around with something else that might cause a problem and you accidentally push it... you can see why in a professional environment with more people and a complicated code base this is bad practice

Once you have staged the changes you want to push, you can then commit
Again, its good to do a "git status" at this point and it should show you what changes are staged
In order to do the next step, which is commit, you can then use "git commit"
Of course its not as simple as just typing "git commit"

Committing takes all of the staged files and commits them with a message, which can be tracked later and is good for seeing who did what when, and why they did it
The proper syntax for this is "git commit -m "your message here"" sorry for the two sets of quotes there but the "" double quotes around the message are absolutely necessary
A commit message is required here by default, and it should say at the very least what changes you did and why. It doesn't have to be anything too complicated or detailed, but it helps if we want to look at an older version or figure out why something is there/happened

Once you have committed locally with your commit message, you are ready to push to the github repo
Of course doing git status here is always good to make sure everything is in the right place

The final step is "git push" 
git push will push the changes you made, with the commit message, to the online repo
If you are on a branch set as upstream, you can simply type "git push" to push these changes. 
Though anything is possible, its generally best to treat this as an action that can not be undone. 
Speaking from experience - both from myself making this mistake and others - its an absolute headache to try and undo this kind of thing

If your branch is not set as upstream, and the branch exists on both your local machine and the online repo, you will have to type "git push origin <branch name>"
For this project its probably best to just set the branch you are working on as upstream

## Pull
Pull is the opposite of push. 
Pulling will update your local repo to look like the main repo; if someone else pushes a change to github, your local version will now be outdated and be behind the github online version. 
In order to make sure your version is up to date, you need to pull down the latest version to your machine.

This should be just like the git push command - "git pull" will pull down the latest version of whatever branch you are on.
If your branch is not set as upstream then you will need to do "git pull origin dev" to do this

## Communicating on pushes and pulls

To avoid conflicts that may and will arise in some capacity, please make sure to do lots of regular small pushes and pulls.
Its good to check the repo for changes and pull every time you start working, to make sure that before you start you have the latest version.
Likewise when you make a small change, or a few small changes its good to push it before you do too much else. This makes it so its easy to identify where issues come from and makes it so you can keep your commit messages concise and still descibe what the changes are. 

Github does a pretty good job of automatically warning you about problems and preventing disasters, so mistakes are likely not going to ruin everything, but keeping a protocol in the process will make things much smoother.

# Pull Requests
The way we move changes from one branch to another - typically this will be happening when moving things from dev to main.
This is something that is done on the github page and is a way for other people to check and approve your changes before they go through.
This is standard and a good thing since its basically a built in peer review step in github and prevents people from putting things straight into main on their own

# Merging Branches
This is how most smaller changes will be moved into a larger branch like dev
Usually you will create your own branch dedicated to the change you are making/thing you are working on in order to avoid conflicting changes
You can make small changes to your own branch little by little, try not to do too many things at once, and when you are ready to put those changes through its good to push them through to the github repo on your own branch, and then merge that branch into dev. 

To do this - lets say you created a branch called "new-feature" which you used to create a new feature for the code
First you make sure you are on that branch and type "git checkout dev" to switch to dev, if this is the place you want to merge to 
Then you can type "git merge new-feature" 
This will merge your "new-feature" branch into the branch you are on, which in this example is "dev"

Do not merge anything directly into main. The reason dev exists and pull requests are there are to have a system with enough checks to make sure anything going to main is okayed and looked over by someone else 

# Undoing Things

I will probably update this soon with instructions on undoing changes, though generally you don't want to
This system is standard and is designed to make sure you go through lots of checks and has lots of safety nets to make sure we don't have to undo anything.
The idea is to be thorough and go forward and do everything possible to avoid going backward. 

Mistakes happen, we may have to try to undo things, but please make sure to follow protocol when working on a group repo. It is a major pain to try and undo things once they are done. 
For example if you push something through to the main branch that should not be there, lets say it breaks everything and slips through the safety checks, and no one catches it, then we are all going to be pushing, pulling, and working on the version of the repo that does not work. While this is most likely going to be fixable, its not ideal to let this situation happen. 

Now that I stressed this I'm sure I'll be the one to somehow break everything.

