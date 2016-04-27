# Tips on Cloning repositories with Git

  Here are some basic tips on cloning repositories, either your own or other public repositories.

## Clone from existing Heroku Apps

  If you are a collaborator on an Heroku app (ie. you created the app or someone added you) then you can access that apps code using the Heroku toolbelt.  In the **Code** section of the Heroku dashboard are details on how to _clone the repository_ using the `heroku git` command.  The `-a` option is for specifying the name of the app you wish to clone.  
  
  For example, if you are a contributor on the sample-play-app, you would clone the Heroku repository using the command:

    heroku git:clone -a sample-play-app

  Once you have cloned the Heroku repository, you can use the usual Git commands.

---

## Cloning from Github repositories

  To get the code from a remote repository, such as Github, we use a command called _clone_.  This takes a complete copy of the Github repository, including all the history of changes.

    git clone <repository-url>

  The above command creates a link in your local repository to the remote repository.  This link is given the alias `origin` by default.  So instead of refering to the cloned repository by its URL, you can use `origin`.
  
  So if you want to get updates from the remote repository you can use the following command:
  
    git pull origin master

  Here we are getting any updates from the remote repositories master branch.


#### Viewing your remote repositories

  You can see which remote repositories are linked to your local repository using the `git remote` command in your local repository.  The following command lists all the remote repositories, their aliases and their full URL:
  
    git remote --verbose


#### Setting your own alias name

  You can also specify your own alias should you wish, either while cloning the repository or using the `git remote` command:
  
    git clone jr0cket <repository-url>
    
    git remote rename origin jr0cket

#### Specifying a directory 
  When you clone a repository, a new directory is created using the name of the remote repository.  So if your repository is called `sample-app-java` then the directory created will also be `sample-app-java`. 
  
  You can also specify the name of the directory the repository is copied into: 

    git clone <sample-app-url> basic-java-app


> **Hint** See the online documentation for [Git Clone](http://git-scm.com/docs/git-clone) for more details
