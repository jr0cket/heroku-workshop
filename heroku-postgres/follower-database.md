# Heroku Postgres Follower databases

  Database replication serves many purposes including increasing read throughput with a master-slave configuration, additional availability with a hot standby, serving as a reporting database, and seamless migrations and upgrades. Though these strategies all serve different purposes they are all based on the ability to create and manage copies of a master (or lead) database. On Heroku Postgres this functionality is exposed as the follow feature.
  
  A database follower is a read-only copy of the master database that stays up-to-date with the master database data. As writes and other data modifications are committed in the master database the changes are streamed, in real-time, to the follower databases.
  
> **Comment** The lag between a master and follower databases varies greatly depending on the amount and frequency of data updates. It is possibile for long running queries on the follower to increase your lag time, though once those queries are done your follower should catch up. Under normal usage it is common for your follower to be within a few seconds or less of your leader.

--- 

> **Hint** See the article on [Creating and Managing Heroku Postgres Follower Databases](https://devcenter.heroku.com/articles/heroku-postgres-follower-databases) for further information.
