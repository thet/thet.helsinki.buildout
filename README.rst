thet.helsinki.buildout
======================

This is the base package of the website for Radio Helsinki - Freies Radio Graz.
It will install all dependencies automatically.

Prerequisite
------------
* Python 2.6 installed. Don't use your Operating System's Python version
  directly. Better create a Sandbox with Virtualenv (see [1]) or use [2].
  
  If you have problems installing Python on your System you may use a buildout
  to build python, like this one [2] (tested on linux and OSX)


Buildout configurations
-----------------------
dev.cfg - Development version
deploy.cfg - Deployment version

How to install
--------------
$ python bootstrap.py -d -c dev.cfg
$ ./bin/buildout -c dev.cfg
$ ./bin/solr-instance start
$ ./bin/instance fg # foreground mode

* Then Point your webbrowser to http://localhost:8080/ (username admin,
  password admin) and install a Plone instance.

References
----------
[1] http://pypi.python.org/pypi/virtualenv
[2] https://svn.plone.org/svn/collective/buildout/bda-naked-python/
