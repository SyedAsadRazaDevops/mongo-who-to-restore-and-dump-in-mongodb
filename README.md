# mongo-who-to-restore-and-dump-in-mongodb

# 1-**create dump**
```
sudo mongodump --db lab_inventory
```
# 2-**convert into  tar**
```
sudo tar –czvf myfolder.tar.gz $home/project/
```
# 3-**extract zip**
```
tar -xf myfolder.tar.gz
```
# 4-**delete databaase in mongo**
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

# 5-**to restore/replace your db to running db**
```
sudo mongorestore --db mydbname --verbose ./usr/local/src/dbackups/mydbdump
```
# 6-**to restore/replace your db to runing db with passing user name and password**
```
sudo mongorestore --port 27017 -u admin -p 'password' --authenticationDatabase admin -d mydbname --verbose ./usr/local/mydbdump
```
# 7-**How to export all collections in MongoDB**
```
mongoexport -u admin -p 'password' --authenticationDatabase -d mydbname -c mycollection -o mybackup.json
```


_________________________________________________________________________________________
link: https://stackoverflow.com/questions/11255630/how-to-export-all-collections-in-mongodb
link: https://www.mongodb.com/docs/compass/current/import-export/
link: https://jelastic.com/blog/remote-access-to-mongodb-in-jelastic-data-import-export/


