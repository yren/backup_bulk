# backup_bulk

## backup and import mediawiki
* backup mediawiki xml
* https://www.mediawiki.org/wiki/Manual:DumpBackup.php
```
/var/www/html# php ./maintenance/dumpBackup.php --full > /var/www/data/wiki_dump_20190325.xml
```

* import backup xml
* https://www.mediawiki.org/wiki/Manual:Importing_XML_dumps

```
php importDump.php --conf ../LocalSettings.php /path_to/dumpfile.xml.gz
# or
php importDump.php < dumpfile.xml
```
access /index.php/Special:AllPages
may need restore /index.php/Main_Page 