
# This is my Cheat Sheet for Postgres Commands

## Terminal Commands

### Manage Databases

#### Create a new Database:

`sudo -u postgres createdb [_DBNAME_]`

#### Delete an existing Database:

`sudo -u postgres dropdb _DBNAME_`

### Manage Postgres itself

##### Show Information about all Clusters

The command below shows meta and status information about all PostgreSQL clusters, including the Postgres version, owners, online/offline status and the directories, where the data and log files are stored.

`pg_lscluster`

