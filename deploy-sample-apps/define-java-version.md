# Define the Java version used 

  So far we have just let Heroku use what ever is the default version of Java.  However we can easily specify a specific version using a `system.properties` file.
  
  The detection of languages and frameworks is done via Heroku Buildpacks, open source scripts that define how a language is detected, assembled and run.  Heroku installs the Java environment automatically when it detects a pom.xml file in the root directory of your project.
  
#### Java versions 

  Heroku installs OpenJDK automatically when a Java appliction is detected.  The versions available are `1.6`, `1.7` and `1.8`.
  
> **Note** Specify a specific version of Java to install for your application 

  Create a new file called `system.properties`.  Edit the file and enter the following:

    java.runtime.version=1.7

  Add the `system.properties` file to your local git repository and push the change to Heroku.
  
    git add system.properties
    git commit -m "defining specific version of Java to install for the application"
    git push heroku master 


--- 

## Alternatively...

> **Hint** All the changes above are also in a branch of the Git repository you initially cloned.  So, as an alternative to the above, you can checkout the branch `java-version` and merge it into the master branch.  Then push the change merged into master to Heroku.

    git checkout java-version
    git checkout master
    git merge java-version
    git push heroku master

