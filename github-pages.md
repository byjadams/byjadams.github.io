---
title: GitHub Pages
layout: page
---

In April 2008 GitHub was co-founded by Tom Preston-Werner. By November 2008, he had the idea of [Blogging Like a Hacker](https://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html) and so created [Jekyll](https://jekyllrb.com/), a static site generator. From there a deeper integration allowed you to have a website that automatically updates with your GitHub repository, [GitHub Pages](https://pages.github.com/).

# Create the repository
Begin by creating a public repository named _username_.github._io_. Two things to note: first, that you must use your username as you would log into GitHub; second, that the URL is `.io` instead of `.com`.

# Clone the repository
Go to the folder where you want to store your project and clone the repository:
```bash
git clone https://github.com/username/username.github.io
```

When cloning an empty repository, GitHub defaults to a remote repo named origin and a branch named main. This is an alternative to initializing a folder on your local machine using `git init -b main` then adding a remote `git remote add origin _https://github.com/username/username.github.io.git_`.

# Setup git client
Since we want to be able to edit files and push them back up to GitHub we have to first setup the git client:
```bash
git config --global user.name "_your name_"
git config --global user.email "_username@example.com_"
```

# Setup GitHub
Since "[support] for password authentication was removed on August 13, 2021", GitHub provides documenation for [Cloning with HTTPS URLs](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls).

You need to generate a personal access token to be used instead of your password.  This is similar to [Google app passwords](https://support.google.com/accounts/answer/185833?hl=en). Another option is to use the Git Credenital Manager (GCM) or similar credential helper. Ideally switch from using HTTP to SSH if you and your organization allow it. Using SSH is standard for developers, comes preinstalled on Mac and Linux systems, and comes with a mature credential helper.

# Hello World
Navigate to the repository and create a new file _index.html_:
```bash
cd _username_.github.io
echo "Hello World" > index.html
```

Add the index.html file to be staged then commit it and push it up to GitHub.
```bash
git add --all
git commit -m "Initial commit"
git push -u origin main
```

# ...and your done!
Now your website is done! Open a browser and go to _https://username.github.io_.
