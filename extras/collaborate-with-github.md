## Collaborating on codebase with Github

  If you want other developers to collaborate on your project, you could add them as a collaborator to your Heroku account.  However this also gives them the ability to deploy updates and change the resources your application is using.
  
  To just collaborate on the codebase, you can use services like Github and either give direct access to your code to other developers or provide an easy way to add changes (ie. pull requests).

> TODO: simplified workflow for using Github with Heroku 

## To collaborate via Github

* Create a new repository on Github

* Add any collaborators you wish using their Github account name (or send them a link to your repository, so the can fork it and send you pull requests).

* Add this new Github repository to your project, run the following within the top level folder of your project (where .git folder lives):

    git remote add git@github.com:account-name/repo-name


* Using `git log` you can to see the state of the repos you have linked to your local repository.  To make this easier to see, you can configure the output of git log to display the commit log.


![Git log commit graph image]()

  You can also use a git tool such as Source Tree (MacOSX) to show off the commit graph

![source tree commit graph image]()

