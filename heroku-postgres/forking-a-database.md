# Forking an Heroku Posgres database 

  Forking creates a new database containing a snapshot of an existing database at the current point in time. Forked databases differ from follower databases in that they do not stay up-to-date with the original database and are themselves writable.

> **Comment** Forking is only supported on production tier database plans. Follow these steps to upgrade from a starter tier (dev or basic) plan to a production plan.

#### Use-cases

  Forked databases provide a risk-free way of working with your production data and schema. For example, they can be used to test new schema migrations or to load test your application on a different database plan. The are also valuable as snapshots of your data at a point-in-time for later analysis or forensics.
  
> **Hint** See the article on [Forking your Heroku Postgress database](https://devcenter.heroku.com/articles/heroku-postgres-fork) for further information.

