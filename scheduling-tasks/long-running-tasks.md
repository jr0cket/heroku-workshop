## Longer running tasks 

  To understand the concept of managing load and scalablity with background tasks and queues, take a look at the Heroku devcenter article [Worker Dynos, Background Jobs and Queueing](https://devcenter.heroku.com/articles/background-jobs-queueing).
  
  There is also an example of how to manage longer running jobs with Java and RabbitMQ in the Heroku dev center article [Asynchronous Web-Worker Model Using RabbitMQ in Java](https://devcenter.heroku.com/articles/asynchronous-web-worker-model-using-rabbitmq-in-java) 

> **Warning** Please remember, adding a `worker` or other backgrond process will increase your dyno usage and therefore you 750 hours monthly credit will not cover the whole month.  Its recommended to set your dynos to zero when not in use for any non production systems.

