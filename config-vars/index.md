# Config Vars

  An application’s configuration is everything that is likely to vary between environments (staging, production, developer environments, etc.). This includes backing services such as databases, credentials, or environment variables that provide some specific information to your application.

  Heroku lets you run your application with a customizable configuration - the configuration sits outside of your application code and can be changed independently of it.
The configuration for an application is stored in config vars. 

For example, here’s how to configure an encryption key for an application:

```
    heroku config:set ENCRYPTION_KEY= my_secret_launch_codes
    Adding config vars and restarting demoapp... done, v14
    ENCRYPTION_KEY: my_secret_launch_codes
```

  At runtime, all of the config vars are exposed as environment variables - so they can be easily extracted programatically.
  
> **Comment** All dynos in an Heorku app will have access to the exact same set of config vars at runtime.

