howto install
=============

debian dependencies
-------------------

$ apt-get install libmysqlclient-dev mysql-server


database preparation
--------------------

* prepare MYSQL database for development
  $ mysql -uroot -p
  mysql> CREATE DATABASE helsinki;
  mysql> CREATE DATABASE helsinki2;
  mysql> CREATE USER helsinki@localhost IDENTIFIED BY helsinki;
  mysql> GRANT ALL PRIVILEGES ON helsinki.* TO helsinki@localhost;
* import dump
  $mysql -uroot -p helsinki < MYSQLDUMP_FROM_SOMEWHERE.sql

* checkout the repository

  readwrite: $ git@github.com:thet/helsinki.buildout.program.git

  readonly: $ git://github.com/thet/helsinki.buildout.program.git


helsinki.program django application standalone install
------------------------------------------------------

* install the application
    $ python-2.6 bootrap.py -d -c helsinki.program.cfg

    $ ./bin/buildout

* create the db
    $ ./bin/django syncdb

* import the data fixtures
    $ ./bin/django loaddata musicfocus
    $ ./bin/django loaddata broadcastformats
    $ ./bin/django loaddata rrules
    $ ./bin/django loaddata showinformation
    $ ./bin/django loaddata showtopics
    $ ./bin/django loaddata hosts
    $ ./bin/django loaddata shows


* run the server
    $ ./bin/django runserver 


http://localhost:8000/program/


[24/Mar/2011 17:23:00] "GET /admin/program/show/ HTTP/1.1" 200 38074
[24/Mar/2011 17:23:00] "GET /admin/jsi18n/ HTTP/1.1" 200 4579
[24/Mar/2011 17:24:06] "GET /admin/program/show/?p=1 HTTP/1.1" 200 10663
[24/Mar/2011 17:24:06] "GET /admin/jsi18n/ HTTP/1.1" 200 4579
[24/Mar/2011 17:24:14] "GET /admin/program/ HTTP/1.1" 200 4834
[24/Mar/2011 17:24:17] "GET /admin/program/programslot/ HTTP/1.1" 200 48592
[24/Mar/2011 17:24:17] "GET /admin/jsi18n/ HTTP/1.1" 200 4579
[24/Mar/2011 17:25:19] "GET /program HTTP/1.1" 301 0
[24/Mar/2011 17:25:19] "GET /program/ HTTP/1.1" 200 5515
[24/Mar/2011 17:26:17] "GET /program/37491/ HTTP/1.1" 200 2082
[24/Mar/2011 17:26:46] "GET /program/23110/ HTTP/1.1" 200 1512
[24/Mar/2011 17:27:05] "GET /program/34568/ HTTP/1.1" 200 942
[24/Mar/2011 17:27:21] "GET /program/recco HTTP/1.1" 404 4065
[24/Mar/2011 17:27:32] "GET /program/recommendations HTTP/1.1" 301 0
[24/Mar/2011 17:27:32] "GET /program/recommendations/ HTTP/1.1" 200 4575
[24/Mar/2011 17:27:54] "GET /program/show/60-minutes-of-vormals-soulfood/ HTTP/1.1" 200 927



