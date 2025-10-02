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
```