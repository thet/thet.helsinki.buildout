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


Upgrade 01/2016
---------------

- Run all upgrade steps
- Delete orphaned js and css
- Delete orphaned import steps
- Run collective.uploadify uninstall step
- Run zettwerk.fullcalendar unstall step

- Run collective.galleria uninstall profile
- Run collective.js.galleria uninstall profile
- Run collective.gallery uninstall profile
- Run collective.configviews uninstall profile

- Run collective.teaser uninstall profile
- Remove "Teaser" from metaTypesNotToList in portal_properties/navtree_properties

- Run LinguaPlone uninstall profile
- Open http://localhost:8080/radio-helsinki/helsinki/@@fix-persistent-utilities and remove all LinguaPlone references.



