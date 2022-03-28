# mongo-who-to-restore-and-dump-in-mongodb

**create dump**
```
sudo mongodump --db lab_inventory
```
**convert into  tar**
```
sudo tar –czvf myfolder.tar.gz $home/project/
```
**extract zip**
```
tar -xf myfolder.tar.gz
```
**delete databaase in mongo**
to onpen mongo terminal/shell
```
mongo
```
to see list of dbs
```
Show dbs
```
"use" __enter your db file name which you used___
```
Use ticket
```
to delete the db
```
db.dropDatabase()
```
QUIT from mongo shell

**to restore/replace your db to running db**
```
sudo mongorestore --db mydbname --verbose ./usr/local/src/dbackups/mydbdump
```
**to restore/replace your db to runing db with passing user name and password**
```
sudo mongorestore --port 27017 -u admin -p 'password' --authenticationDatabase admin -d mydbname --verbose ./usr/local/mydbdump
```
**How to export all collections in MongoDB**
```
mongoexport -u admin -p 'password' --authenticationDatabase -d mydbname -c mycollection -o mybackup.json
```


_________________________________________________________________________________________
link: https://stackoverflow.com/questions/11255630/how-to-export-all-collections-in-mongodb


