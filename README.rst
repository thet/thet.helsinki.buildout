thet.helsinki.buildout
======================

Buildout for Radio Helsinki - Freies Radio Graz.

Prerequisite
------------

- Python 2.7
- Virtualenv
  
Install
-------

::
    $ virtualenv .
    $ ./bin/pip intall -U setuptools pip zc.buildout
    $ ./bin/buildout -c dev.cfg  # for Development
or::
    $ ./bin/buildout -c deploy.cfg  # for live installation

Start
-----

::

    $ ./bin/zeoserver start
    $ ./bin/instance fg
    $ google-chrome http://localhost:8080/

