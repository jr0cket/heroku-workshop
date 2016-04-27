# Scaling apps via the Heroku toolbelt 

> **Note** Scale the dynos for yor Heroku application using the toolbelt.  At the same time, view the live Heroku logs so you can see exactly what is happening.

  First, check how many dynos are running using the Heroku toolbelt:

```
    heroku ps 
```

![Heroku toolbelt - list processes](../images/heroku-toolbelt-processes.png)

  Now scale your application to run 3 dynos

``` 
    heroku ps:scale web=3
```

![Heroku toolbelt - scale to 3 web process dynos](../images/heroku-toolbelt-process-scale-to-3.png)

  In the Heroku logs you can see additional web processes being provisioned automatically.  The new dynos come almost instantly and are fully active as soon as your application process has started.  

![Heroku log - scalaing up dynos](../images/heroku-log-scaling-dynos-1-to-3.png)

> **Comment** The faster you application process starts, the faster you get new dynos.


  Now scale down your application back to 1 dyno: 

![Heroku toolbelt - scal to 1 web process dyno](../images/heroku-toolbelt-process-scale-to-1.png)

  You can see how quickly the excess dynos are shut down, again affected by how quickly your application exits.

![Heroku log - scaling down dynos](../images/heroku-log-scaling-dynos-3-to-1.png)


### Resizing your dynos 

  You can resize to a larger or smaller dyno type using the toolbelt.
  
> **Warning**  Remember that larger dynos will use up your monthly free credits faster, so dont forget to resize down and set your dyno usage to zero.

```  
  heroku ps:resize web=2x
```

![Heroku toolbelt - resize dyno to 2X](../images/heroku-toolbelt-process-resize-to-2x.png)

  Now scale down the dyno back to the original 1x size

```
    heroku ps:resize web=1x
```

![Heroku toolbelt - resize dyno to 1X](../images/heroku-toolbelt-process-resize-to-1x.png)

  Finally, scale your dynos down to zero:
  
    heroku ps:scale web=0


