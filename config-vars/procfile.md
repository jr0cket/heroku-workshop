# Configuration Variables in the Procfile 

  You can use configuration variables in the Procfile.  Common examples are database connections or port numbers for listening for web traffic. 


## Setting a PORT variable 

  You cannot specify the port number your application listens to, as Heroku may need to change this to provide you a consistent compute resources for your app.  Instead you can use the environment variable PORT to ask Heroku for the current port number.
  
  This PORT variable is usually used in either the Procfile when defining your process or in the configuration file for your application.
  
  See the [Java process examples](java-process-examples.html) section to see how this is used in the Procfile.

## Java options 

  The JAVA_OPTS configuration variable defines memory settings for the Java Virtual Machine your application runs in.  You can see an example of how to use this in the sample Java application:

    web: java $JAVA_OPTS -cp target/classes:target/dependency/* Main


  The default JAVA_OPTS values vary depending on the size of the dyno you are deploying onto:

| Dyno | Max Heap size | Initial Nursry Heap size | Initial Heap size | Thread stack size |
| -- | -- | -- | -- | -- |
| `1X` | -Xmx384m |          |          | -Xss512k |
| `2X` | -Xmx768m | -Xmn192m | -Xms768m |          |
| `PX` | -Xmx4g   | -Xmn2g   | -Xms4g   |          |

  Additional JVM flags can be used to monitor resource usage in a dyno. The following flags are recommended for monitoring resource usage:

    -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+PrintTenuringDistribution -XX:+UseConcMarkSweepGC

See the [Heroku Java troubleshooting article](https://devcenter.heroku.com/articles/java-memory-issues) for more information about tuning a JVM process.

> **Hint** To understand more about Java flags and options, run the command `java -X`

