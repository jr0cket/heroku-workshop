# Deployable Apps



> **fixme** This secion needs a lot of work

As developers got more into testing code (unit testing, acceptance testing) then generally code was create that was easier to test.  Frameworks evolved to help with different aspects of testing (eg. mocking).

Now developers are getting more into DevOps, application are starting to be designed that are more deployable.

So what are the aspects of a deployable app ?


## 12 Factors

Select some of the most relevant bits from 12 factors




## Heroku Deploy a Lot Happens in 1 Minute
As technology progresses then taking a few minutes to deploy your app can seem like a long time, but when you consider everything Heroku is doing during that time then its quite amazing

### Provision server resources & managing traffic

Heroku creates a new “server” each time you deploy, so that the currently live application can still handle reuests until the new version is ready. Rather than a whole bloated server, Heroku actually creates a new Linux container with a running OS. This Linux container usually takes a second or less to create with a running operating system.

### The environment is then established

Every language you use to write your application needs some kind of runtime, eg. if you need Java you need the JVM, Ruby apps need a particular version of Ruby, Javascript probably needs nodejs and PHP needs a webserver. As part of the Heroku buildpack used during the deployment, the relevant libraries and platforms are brought in. Unless you change the configuration of your build or the buildfile you use, Heroku will always bring in the same version of the environment you need to run your app each time you deploy.

### Compilation of code

If your app is compiled, then the build process is run so you have a deployment made from your standard production build.

Environment variables are set for the applications and any services (caching, logging, monitoring, etc) or datastores (postgres, redis, mongodb) are therefore automatically connected too.

All the relevant processes are run and scalled (can you scale your app to a certain level when you deploy)

