# Deploy a branch other than Master

  When you push code to Heroku, you must always push it to the `master` branch if you want your code to be deployed.  You can of course push any branch to Heroku.
  
  For example, if you have a branch called `dev`, you can deploy the code in that branch as a new app using the commmand
  
    git push heroku dev:master

  This will push your `dev` branch in your local Git repository to the `master` branch on Heroku.  Then Heroku will deploy that new version.
  
  If you are going to push a branch, you should also consider creating a new Heroku app for that branch, especially when you are working in teams.  So instead of just pushing the `dev` branch, you would:
  
    # Create a new Heroku app
    heroku create my-app-branchname
    
    # Push & deploy your branch 
    git push my-app-branchname dev:master


> **Comment** If you push a branch other than `master` to Heroku, the push will be successful, however you will not trigger the deployment process for the code in that branch.  A new version of your app will not be created or deployed.

