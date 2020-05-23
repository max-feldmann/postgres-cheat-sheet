
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

`pg_lscluster`

#### Create a New Postgres User

The Command below will start an interactive "Gui" that allows you to create a new User and set its role (Superuser yes or no).

`sudo -u postgres createuser --interactive`

#### Enter Postgres Promt w/ Username

User "psql" to enter postgres prompt with standard postgres user.

`sudo -u postgres [username]` 

## Postgres Prompts

Leaving Postgres Command Line

`\q`

Create a Database

`CREATE DATABASE [Databasename];`

Connect to Database
Run the Psql Program giving it the name of the DB we want to connect to.

`psql [Databasename]`

List the tables

`\d`

DESCRIBE a single table

`\d [Tablename]`

