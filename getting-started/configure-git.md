# Configure Git with name and email

  When you install the Heroku toolbelt it includes a Git client.  You can also use any other git client you want, either command line or graphical tool.

  You should identify yourself to Git before carrying out any commits.  To identify yourself you specify a name and email address (the email you registered with Heroku preferably).

  To add your git name and email, either edit the **~/.gitconfig** file or run the following two commands:

    git config --global user.name "your name"
    git config --global user.email "your.name@domain.com"

  To check what has already been added to Git (some gui clients add information), you can list all the current configuration entries:

    git config --list

  If you are still finding your way with Git, take a look at the seperate [Git tutorial](http://jr0cket.co.uk/git-workshop/) or [try.github.io](http://try.github.io)
  
