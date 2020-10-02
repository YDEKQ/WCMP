# WCMP
Windows+ Caddy2+ PHP+ MySQL ALL-in-1 Portable Package

![image](https://github.com/jiix/WCMP/raw/main/wcmp1.jpg)

“ALL-in-One” 1-click windows webserver using Caddy2+php+MySQL (like XAMPP or WAMP) for quick test site development (or for production if you like, there are no artificial performance limits). Open-source.

Unzip and it is ready in 5 seconds. Fully portable. Take the server + websites anywhere you go.

(It also makes the server-moving / full-site-backup much easier, simply copy/paste/move this folder to somewhere else, run again and everything will follow)

![image](https://github.com/jiix/WCMP/raw/main/wcmp2.jpg)

Simply run WCMP.exe And you now have a webserver+php+database environment for your quick web application development. (full function wordpress tested)

## version
* Caddy v2.2.0
* PHP v7.4.11
* MariaDB v10.4
* SQLite v3.31.1
* phpMyAdmin v5.0.2

## Notes:

1. All the included programs are the latest x64 version binaries (May 2020) fetched from the official site, all original. All credit and copyright go to their amazing developers. And I don’t reserve any rights to this little tool.

2. All The configurations are mostly “factory default” with little performance modification, good enough for personal blogs and medium-size projects.

    * Caddyfile link to php port 9000 (default, you can not change) for php fastcgi;
    * php.ini link to mysql port 3306(default, you can change). Some PHP extensions enabled for wordpress to run;
    * Everything is using “relative path”, so the whole package is portable;
    * Database username root, empty password (mariadb default), change it as you like;
    * The phpmyadmin is the default site01. You can use it to create new databases or change root password etc. when you first time visit http://127.0.0.1

3. If you replace the programs inside the sub-folders to other versions (eg. php5 replace php7, MySQL replace MariaDB) they should work fine (keep the config files if you are not sure how to setup properly)

## Exp😄
Setup a wordpress site in 5 minutes guide:
1. run this tool, go to http://127.0.0.1 (It is PHPMyAdmin initially), log in using database username:root, password [empty]
2. click [Databases] section -> Create database, database name type in: wordpress01, and pick {utf8mb4_unicode_ci} from dropdown, and click create.
3. download wordpress.zip, un-zip wordpress into this-tool\www\site01 folder (you can delete everything was inside there first)
4. visit http://127.0.0.1 again, you should see the "wordpress installation" page. Using the information above to finish the setup
(In case you want your site to go internet public, you'd better change the database root password to something secret in PHPMyAdmin, and update caddyfile ":80" to "yoursite.com")

## (⊙﹏⊙)
Fork from https://kknbb.com/stories/wcmp-windowscaddy2phpmysql-all-in-1-portable-package/
