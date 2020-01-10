---
title: How to setup Github
subtitle: Cheatsheet
author: Rogelio Prieto Alvarado
date: 9/enero/2020
---

# steps to synchronyze a github folder

1 . Go to your local folder, example:

```bash
cd ~/github/markdown/myfolder
```

2. Specify to your computer that ```myfolder``` is a directory managed by the ```git```, enter:

```bash
git init
```

3.  Next, you specify to ```git```  you care about all files and want to track any changes from this point and forward, enter:

```bash
git add *
```

**Optional**: you can create a ```README.md``` file and specify to ```git``` to care only about this file.

```bash
git add README.md
```

4. Make a commit

```bash
git commit -m "my first commit"
```

5. Connect your GitHub repository with your computer

```bash
git remote add origin https://github.com/<your_username>/<repository_name>
```

Explaining this command step by step. We are telling ```git``` to add a remote called origin with the address https://github.com/<your_username>/myfolder.git (i.e., the URL of your git repository on ```GitHub.com```).  This allows you to interact with your Git repository on GitHub.com by typing origin instead of the full URL and Git will know where to send your code. Why origin? Well, you can name it anything else if you'd like.

6. Now that we have added the remote, we can push our code (i.e., upload our README.md file) to GitHub.com.

```bash
push -u origin master
```

# How to ignore local changes and replace them with remote files

Discard all local files and download the remote files.

```bash
git reset --hard
```

# Restore a file with the remote file version.

```bash
git checkout --filename
```

# References

Source by: <https://opensource.com/article/18/1/step-step-guide-git>


