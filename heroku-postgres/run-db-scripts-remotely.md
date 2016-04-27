# Run Db scripts remotely


  Your remote job will run on a 1x dyno by default.  This should be enough for most scripts, however if you need more compute resources to run your script faster or need more memory, then you can specify the size of the resource you want

    heroku run --size=P2 pg-medium-sized-script
    
    heroku run --size=PX pg-intensive-script

