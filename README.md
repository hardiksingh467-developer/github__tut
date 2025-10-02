# GIT and GITHUB AND VCS(Version Control System)
This repository contains tutorial and future learning about Github


```
Version Control System also known as Source Control System, is a tracking and managing software used for managing file changes

Famous known VCS :-
Git
Apache Subversion
Piper

Overtime our codebase can be changed to deal with such situation we used such softwares to save and maintain its timeline

To download Git we need to go to the website: https://git-scm.com, where scm stands for source control management

click on downloads and choose for your OS

open a terminal and execute the command: git
we can now see an ocean of commands that git comes with
execute the command: git --version
this will let you know the git version installed on your machine
```

```
Now after we have successfully installed Git, we will now config the Git
We will tell GIT about our name, email, etc...

This is because, let's say we are working in a big company and we are contributing to the codebase, GIT needs to a way to uniquely identify us to allow others to know who added the particular lines in the codebase

we execute the command: git config --global user.name
the above command will let us know the name of the global user
we execute the command: git config --global user.name "Hardik Singh"

Similarly we can setup our email too
```

### Version Controlling with git
```

When we create a new file let's say index.js and we add some code into it
Now currently at this point we are not tracking the file

To start tracking the folder we need to initialize GIT,
To Initialize GIT :- 
In the terminal we first navigate inside the folder
then execute the command: git init
the above command initializes GIT in the current directory
In VSCode in front of file in the sidebar, we can see that there is a U in front of the filename
This `U` stands for untracked
also initializing GIT will create a hidden .git folder
All the tracking that is to be followed will now be stored in this folder
Make sure not to mess with it

Now to track this Untracked file, execute command: git add index.js
The above command will make git start tracking index.js, and we can see that `U` has now changed to `A`, 

If we execute command: git diff
It will show in the terminal, the lines that were CREATED and DELETED

If we add another file let's say, script.js, we will see that this file is now being tracked
and now we need to repeat the above process

But in reality, we will have a lot of files and adding each file for tracking will become a tedious task
So to add all the files in a directory to tracking we execute the command: git add .

Lets say we added a file or a directory to tracking by mistake we can use command: git rm ./node_modules

```

#### Now let's track the timeline of our codebase over an hour, day and a week(COMMIT)
```
Let's say we are tracking a directory and we believe that the changes we needed to implement are done

Now we will save the current state of the directory by committing the code
It is like a checkpoint

To commit our current state of directory we will say: git commit -m "message around the checkpoint for better developer experience"
The above command will CREATE a commit

To READ the list of recent commits, execute command: git log
The above command will list the commits along with their id, author, datetime and message

Let's change the code a little bit, maybe for now we add a comment and commit the code again

Our Code has now transition from initial commit to the current commit

If we execute command, git log --one-line
The above command will show the list of our commits, only this time the unique ID assigned to our commit will be shortened to 5 characters

Now if we copy those Five characters and execute command: git show <those_5_characters>
The above command will show the changes that exist as compared to it's initial commit

We can execute another command: git blame <file__path>
The above command will show line by line, that which line of code was written by whom



Always work on one functionality and commit the changes , do not commit all the changes at once
Learn to have a clean commit history
```


### Staging Area
```
Let's say we added some changes in our file
Now executing: git diff
will show us our additions

Now in our terminal if we execute the command: git status
The above command will show the filename which has been modified after the recent commit

Committing right now will not work , as our `STAGING AREA` is empty
So we first need to take these files into our staging area

To take our files to staging area we use command: git add .

Now we can again commit our changes
```


### Reverting back to previous commit
```
Reverting back is a functionality to revert back to the precious checkpoint or commit if something goes wrong

For that we first need to develop an understanding of HEAD
As we know what is a linked list, in a linked list, the latest node is referred to as HEAD

And if we take a look at our commit history we can see the resemblance of Linked List
Our HEAD is the latest commit in our commit history

Now let's say the code right now as we are in HEAD, is faulty and breaks the production

If we point our HEAD to previous commit history, we can say that we reverted back to our previous codebase

if we use command: git reset --hard <ID__of__5__characters>
It will shift our HEAD to the commit of the ID we provided
After this we have now officially lost our HEAD

But let's say this is not how we want to deal with this faulty code situation
Let's say we just want to change the particular code
Let's say the fault was in the second commit we ever made, but now there has been hundred's of commit

If we execute command: git revert <ID__of__5__characters>
The above command will add everything that was removed as compared to the commit after that and remove everything that was added as compared the commit before that

Now commit the new changes
```


### GIT and GITHUB