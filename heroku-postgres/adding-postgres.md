# Adding Postgres 

  Heroku Postgres is one of many services you can provision from [addons.heroku.com](https://addons.heroku.com).  Just like other addons, you can add Heroku Postgress via the Heroku Dashboard or via the Heroku Toolbelt.
  
![Heroku Dashboard - Heroku Postgres](../images/heroku-dashboard-addons-heroku-postgres.png)  

> **Comment** There is no need to add Heroku Postgres to a Java app, this is done automatically by the Java buildpack.

#### Adding a Backup - PG Backups

![Heroku Dashboard - addons - PG Backups](../images/heroku-dashboard-addons-pg-backups-banner.png)

  PG Backups is a service that captures and restores backups from your Heroku Postgres databases for an application. PG Backups imports data from an existing database backup, and exports backups for off-site storage

  Just like other addons you can provision PG Backups via the dashboard or toolbelt.

![Heroku Dashboard - addons - PG Backups add](../images/heroku-dashboard-addons-pg-backups-add.png)

> **Note** Add the PG Backups service to your application 

---

> **Hint** See [Importing & Exporting Heroku databases with PG Backups](https://devcenter.heroku.com/articles/heroku-postgres-import-export) article for further details.

