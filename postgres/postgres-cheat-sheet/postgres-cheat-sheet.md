
# This is my Cheat Sheet for Postgres Commands (Using Ubuntu)

## Terminal Commands

### Manage Databases

#### Create a new Database:

`sudo -u postgres createdb [_DBNAME_]`

#### Delete an existing Database:

`sudo -u postgres dropdb _DBNAME_`

### Manage Postgres itself

#### Show Information about all Clusters

The command below shows meta and status information about all PostgreSQL clusters, including the Postgres version, owners, online/offline status and the directories, where the data and log files are stored.

`pg_lsclusters`

#### (Re)Start a Cluster

Sometimes you will get an error-message like that:

`psql: could not connect to server: No such file or directory
        Is the server running locally and accepting
        connections on Unix domain socket "/var/run/postgresql/.s.PGSQL.5432"`

It basically means, that the cluster, you want to work with, is down and needs to be started.

`pg_lsclusters` wil show you which cluster is down and needs to be started.

Then go

`sudo pg_ctlcluster <version> <cluster> <action>`

For example

`sudo pg_ctlcluster 10 main start`

#### Create a New Postgres User

The Command below will start an interactive "Gui" that allows you to create a new User and set its role (Superuser yes or no).

`sudo -u postgres createuser --interactive`

#### Enter Postgres Promt w/ Username

User "psql" to enter postgres prompt with standard postgres user.

`sudo -u postgres [username]` 

## Postgres Prompts

### LEAVING POSTGRES Command Line

`\q`

### CREATE a Database

`CREATE DATABASE [Databasename];`

### CONNECT to Database
Run the Psql Program giving it the name of the DB we want to connect to.

`psql [Databasename]`

### LIST the tables

`\d`

### DESCRIBE a single table

`\d [Tablename]`

### LIST the data bases