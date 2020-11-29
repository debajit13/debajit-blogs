---
title: Deep Dive Into Git(Part II)
date: "2020-10-17T23:46:37.121Z"
description: In my previous blog, I discussed “what is Git?”. In this blog, I am going to share how you can get started with git commands.
---

Before deep dive into git, firstly, we need to understand what is GitHub. So GitHub is a code hosting platform for collaboration and version control. There are many platforms same as GitHub like GitLab, Bitbucket etc.

Before getting started, we need to install git. To install git just go to the [link](https://git-scm.com/downloads) and download git for your system. If you are using windows then you have to install git bash. If you are using Linux or Mac then the default terminal is fine for you. After that, you need to go to [GitHub](https://github.com/) and create an account. In this article, we are mainly focusing on git commands. Now we can start our journey with basic git commands.

First, we need to understand some of the words that are often used in git.

1. repository: A git repository is a .git folder inside a folder.
1. sha/hash: It is a hexadecimal number which is used to identify different commits.
1. directory: It is same as a folder. But when we navigate through terminal we use the term directory.
1. master/ main: It is the name of the default branch in git.

Now, just open git bash if you are in Windows and terminal if you are in Mac or Linux. Every git command started with git keyword. So to check that git is installed properly in your system just run the following command:

> git — version

![git version check](https://miro.medium.com/max/333/1*Y-VZAtal28cu5lQQH4FNUw.png)

It will show you the version of git you installed in your system. After that, you have to configure your name and mail at git bash. To do that run the command:

> git config — global user.name “your name”

> git config — global user.email “your email”

![git name and mail config](https://miro.medium.com/max/700/1*TYepG31WSj7Nb0NGSOpnzA.png)

Now you are ready to go. First, you have to create a directory. To create a directory using terminal use the following command:

> mkdir folder-name

To enter inside a directory write the following command:

> cd folder-name

![create and enter directory](https://miro.medium.com/max/307/1*pn6Oz-Stx-WNZR99_S2qsA.png)

After entering into the directory, now you have to initialize git to access all the features of it. use the following command:

> git init

![git init](https://miro.medium.com/max/636/1*CLb2qYTtBZaWxW8tBpQcpw.png)

It initializes an empty git repository. So now if you turn on hidden files and folder, you can find a .git folder inside that folder. Or you can use

> ls -a

command and you can find one .git folder inside it. It is the place where git controls all of its features.

Now you have to insert some contents inside the directory. So just open that directory in your favourite editor(Ex: VScode, Atom, Sublime etc.) and write some codes inside it.

![write some code](https://miro.medium.com/max/700/1*CMQBFYE9RkLRx5i7s0jkdA.png)

After saving all the files. Now you need to stage all the changes inside the files. Because now the files are inside the directory but version control does not work now. Only the last saved version was shown now. To stage all the changes use:

> git add file-name (to stage changes only inside that particular file) or,

> git add . (to stage all changes inside the current directory)

![git add filename](https://miro.medium.com/max/418/1*kwcG-eaMQLcEp1xwqipH8g.png)

Now after staging all the files or changes inside the project you need to commit those changes. If you don’t commit those changes then only the last version is saved. To commit all the changes that you made use the following command:

> git commit -m “commit message”

![git commit -m message](https://miro.medium.com/max/713/1*5IZBGBsL3M2pk4fd8FyHVQ.png)

You can also add and commit both at the same time by using the command:

> git commit -a -m “commit message”

After committing all the changes a sha or hash is generated for that particular commit. Now if you made some more changes then you can compare those changes with any committed versions by using the command:

> git diff sha-of-one-commit sha-of-another-commit -p

![git diff](https://miro.medium.com/max/746/1*8tWSCjKx9qcnS5MlQwEi6A.png)

One of the most helpful git command is status. It gives you all the information about the current situation of your repository.

> git status

![git status](https://miro.medium.com/max/856/1*yPA_EJqQdalfsp8_wliQfw.png)

###What is HEAD?
HEAD is a pointer which always points to the last committed version. So you can also use the HEAD in your commands. Ex:

> git diff HEAD HEAD~1 -p

![HEAD example](https://miro.medium.com/max/576/1*u57RpLNNoGuwMFppk0JyCA.png)

To list all the commits details use the following command:

> git log

![git log](https://miro.medium.com/max/855/1*zqaSdGRktbkixgsmFXw7tg.png)

Another useful command is show command. It is like a merge of git diff and git log. By using show you get all the details of a particular commit like author, date and so much more.

> git show sha-of-the-commit

![git show](https://miro.medium.com/max/671/1*EVeT7xq1hJHppyRXoY_-qg.png)

To see the commits in a particular file use:

> git annotate file-name

![git annotate filname](https://miro.medium.com/max/875/1*o5muOgHT18mqSr95U0eNOg.png)

If you are using VScode then you can also you an extension named as git lens to get the same output in VScode.

Now if make some changes but not add them to go back to the last committed version use:

> git checkout — filename

![git checkout -- filename](https://miro.medium.com/max/659/1*0lztOUGP62lCoODs6ixBBw.png)

If you add those changes and now want to go back, just use reset command:

> git reset HEAD filename

![git reset HEAD filename](https://miro.medium.com/max/658/1*FO7GbIoCetr2N0zB-OZ9oQ.png)

Now if you run the checkout command it takes you to the last committed version.

If you are in a stage when you commit those changes and find that you are doing
something wrong then just go to a previous version write

> git checkout sha-of-the-commit-you-want-to-go file-name

![git checkout sha-of-where-you-want-to-go filename](https://miro.medium.com/max/755/1*DcJ4fYnF5nnIMZqzWrVqeg.png)

These are the basic commands of git. After learning about all these commands you are ready to go with GitHub and other complex commands of git. Just check out any cheatsheet of git for learning more.
