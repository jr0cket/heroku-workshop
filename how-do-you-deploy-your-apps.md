# How do you deploy your apps

  Do you know the process required to deploy your application, or do you build it and hand it over to an operations team?  
  
  The less you know about the deployment process, the more issues the deployment of your app is likely to have.  However as a developer, you dont want to divert a lot of time to deployment and other operational tasks as you have lots of development to do already.

  Lets look at some typical process of deployment, highlighting common issues along the way.

#### Your own data centre 

  You may have a very well organised IT operations team that have the deployment process for your app very well defined and even automated.  However, many IT operations teams have a 6 months plus backlog of work, so not everything gets as automated as it could. 
  
  Deploying to your own data center can can take time and several tries to get your application deployed successfully.  Some of the issues you may experience are:
  
  * IT operations teams are not familiar with the workings of your application, so weary about putting it into production until they know a lot more about it.
  * Detailed documentation about your application is often required
  * Approval processes to follow, including the passing of a review board who decide if your applicaiton can and should be deployed and on what time table.
  * Developers have no say in when an application will be deployed.
  * No tests in place to confirm your application has deployed successfully and is working as expected, so a developer needs to create these
  * Dry runs required - a developer and ops person walk through the deployment to ensure the ops person is happy with the deployment process.  This is often time intensive, especially if the deployment is not scripted.  Also need to wait for an ops person to be available for the dry run
  * Deployment is often a manual process - if not documented in detail is easy to miss steps and have a failed build.
  * Software Tools are not available in production
  * Dependencies are not installed in production
  * Different operating system versions or patch levels



#### Hosting company

  Using a hosting company is different from your own data center in that the ops team you have to work with will be remote and you probably have limited communication with them except email or an issue tracking system.
  
  You may experience the same issues deploying here as with your data centre.

#### Cloud - Infrastructure as a Service 

  The challenge as a developer is that you often end up doing a lot of IT operations work, rather than getting on and developing your app.
  
  * Still working with servers and they need regular maintenance and management

#### Cloud - Platform as a service 


Advantages
  * The infrastructure is fully managed, so you should not need to maintain the operating system, network routing, loadbalancing or any other troubleshooting 

#### Characteristics of your deployment 

  Your deployment should not have any dependency on the underlying operating system or tools - it will be harder to maintain a consistent deployment process if you rely on aspects of the operating system that could easily change without you knowing (security patches, OS updates, new build processthat deploys different components of the operating system, etc).

  The deployment process should be documented so everyone knows how it works, however the deployment process should be as automated as possible to avoid human error.  This will create a highly repeatable process
  
  The deployment process should log details of every step taking, preferably in one place so you can easily track down issues and understant the root cause of any problems quickly.
  
  There should be a robust rollback proceedure, again as automated as possible, with full details being logged so that a root cause analysis can be done.

> **Hint** See the [12 Factor guide](http://12factor.net) for more details on creating deployable applications

---
_Last updated: Mon 12 Jan 2015 08:51:49 GMT_
