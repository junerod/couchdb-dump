couchdb-dump (& restore)
============

**Bash command line script(s) to EASILY dump&restore a couchdb database and/or to restore it.**

When launched it takes as arguments:

* url of database (without http://)
* database name
 
NB: Dumped database is outputted in the stdout (screen)

## Why do you need it?
Surprisingly there is not a straightforward way to dump a couchdb database. Often you are suggested to replicate it or to dump it with the couchdb `_all_docs` directive. 

**But using `_all_docs` directive you have as output a JSON object which cannot be used to directly re-upload the database to couchdb**.

Hence, the goal of this script(s) is to give you a simple way to download & upload your couchdb database.


## DUMP Usage

Just write in the command line:

*bash couchdb-dump DB_URL... DB_NAME...*

  `DB_URL`: the url of the couchdb instance without 'http://', e.g. mycouch.com
  
  `DB_NAME`: name of the database, e.g. 'my-db'


### Examples

*bash coucdb-dump mycouch.com my-db*

**Saving output to file**

*bash coucdb-dump mycouch.com my-db > dumped-db.txt*


## Restoring the database


