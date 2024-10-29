Setting up GitHub Pages
=======================

To have a website that automatically updates with your GitHub repository, GitHub has created Jekyll then packaged it together into an offering [GitHub Pages](https://pages.github.com/).

# Create the repository
Begin by creating a public repository named _username_.github._io_. Two things to note: first, that you must use your username as you would log into GitHub; second, that the URL is `.io` instead of `.com`.

# Clone the repository
Go to the folder where you want to store your project, and clone the repository:
```
$ git clone https://github.com/username/username.github.io
$ cd _username_.github.io
```

When cloning an empty repository, GitHub defaults to a remote repo named origin and a branch named main. This is an alternative to initializing a folder on your local machine using `git init -b main` then adding a remote `git remote add origin _https://github.com/username/username.github.io.git_`.

# Setup git client
Since we want to be able to edit files and push them back up to GitHub we have to first setup the git client:
```
$ git config --global user.name "_your name_"
$ git config --global user.email "_username@example.com_"
```

# Setup GitHub
Since "[support] for password authentication was removed on August 13, 2021", GitHub provides documenation for [Clonging with HTTPS URLs](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls).

You need to generate a personal access token to be used instead of your password.  This is similar to [Google app passwords](https://support.google.com/accounts/answer/185833?hl=en). Another option is to use the Git Credenital Manager (GCM) or similar credential helper. Ideally switch from using HTTP to SSH if you and your organization allow it. Using SSH is standard for developers, comes preinstalled on Mac and Linux systems, and comes with a mature credential helper.

# Hello World
Create a new file _index.html_:
`$ echo "Hello World" > index.html`

Add the index.html file to be staged then commit it and push it up to GitHub.
```
$ git add --all
$ git commit -m "Initial commit"
$ git push -u origin main
```

# ...and your done!
Now your website is done! Open a browser and go to _https://username.github.io_.
