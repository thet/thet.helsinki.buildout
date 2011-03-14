===========================
Radio Helsinki Website TODO
===========================

ie html5 javascript not needed ATM
----------------------------------
  <!--[if lt IE 9]>
  <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
  <![endif]-->



WHAT NEXT?
==========

OK * teaser und projekt - selbes icon - ändern
OK * ical/vcal bei projekten rausnehmen
* suche: suchseite soll mit wildcards funktionieren.
* benutzer: wegschalten
* benutzer: keine rechte projekte anzulegen?
* kalenderblatt - not styled
* projekte: kein hinzüfügen menü?


openid login
------------
http://ldap.helsinki.at:8000/
http://ldap.helsinki.at:8000/login
http://ldap.helsinki.at:8000/id/thet


programmverwaltung
------------------
OK * dateutil: daily option
* ceiiling date for recurrence?

easy 1 .. 3 hard
* deliverance integration 10h
* week view           3
* day view            3
* calendar block      2
* now playing         2
* programmhinweise    2
* filtermöglichkeiten 2
* solr integration    1
* disqus integration  1

* evtl rss feeds      2
* evtl ical downloads 3
* WYSIWYG editor integration für textfelder (am besten tinyMCE).


vt plone basierte lösung
------------------------
* gleiches eingabeinterface
* gleicher login
* kommentare direkt helsinki.at
* bessere verlinkungsmöglichkeiten.. referenzieren von objekten

nt plone basierte lösung
------------------------
* plone.app.event recurrence = voraussetzung. jquery.recurrenceplugin fehlt
  noch.
* langsamer


cms
---
OK * teaser titel umlaute utf error
* teaser edit screen importance discplays only number:
* https login
* users, groups, rights and config

* livestream: collective.nakedviews -> views without plone context

* configure c.gallery to use correct sizes

OK * livestream seite
* now playing

OK * find a place to put news items in. configure display of news items.
* find a place to put teasers in.
OK * show main teaser on correct place
* configure all content types, if they don't look appropriate.

OK * make an "available" adapter for portlets. e.g. adapt context,manager,... show portlet only if context = ISite
* collective.folderishtypes: let CT derive all other interfaces too... currently they are overwritten.
* backport changes to folder_listing and folder_summary_view to plone

OK * configure folderishtraverse for project/aktuelles

OK * configure portlets display on right/left side
Ok * navigation
    don't show current item in path, if it's in typesNotToList
    navtree_properties --> showAllParents = False

Portlet configuration
=====================

all
---
left:
    navigation portlet
    recent
    revisions

startsite news
--------------
left:
    teaser portlet
    programm derzeit
    sendungen zum nachhören
       rss portlet 1
       rss portlet 2
    programmhinweise

right:
    "unterstütze uns"
    "find us on facebook"
    "mach mit"

any subsite
-----------
right:
    teaser portlet
    social bookmarks portlet

programm
--------
left:
    programmkalender
    programmhinweise
    (programmfilter)

right:
    legende

projekte
--------
left:
    navigationsportlet 2 - projekte

info
----
right:
    gallery portlet


content types
=============
additional
----------
OK * project
OK * teaser

OK * gallery -> folder with album/gallery view

standard
--------
* news item
* page
* event
* folder
* image
* file

portlets / viewlets
-------------------
OK * collective.gallery
OK  - display all subfolders with galleryview enabled
OK  - searchpath: portal_root, context

OK * RSS freieradios
  http://www.freie-radios.net/portal/podcast.php?radio=43&rss
OK * RSS cba
  http://cba.fro.at/stationsrss/4

OK * social bookmarks
  + bookmarks frei wählbar + sortierbar
  + bookmark service frei wählbar
  + eigener bookmark service

* tagcloud / filter

OK * banner
  content type: Teaser, teaser
    - image
    - alternative image (other layout)
    X folderish: images, files
    - text: richtextwidget
    - link: reference, href
    - from, until dates
    - importance: 1,2,3,4,5
  portlet collective.teaser.portlet, teaser_portlet
    - show importance levels: multiselection
    - prefer altimage
    - image layout
    werden mehrere teaser portlets angezeigt, sollen in allen unterschiedliche teaser angezeigt werden oder gar nicht. teaser id kann über REQUEST var gesetzt werden.


ADDONS OVERVIEW
===============
OK * alm.solrindex
OK * plone.app.discussion
OK * collective.disqus

OK * collective.folderishtypes
OK * collective.folderishtraverse
OK * Products.LinguaPlone
OK * zettwerk.fullcalendar
OK * collective.flowplayer
OK * collective.gallery
OK * collective.uploadify
NO * collective.quickupload
* ...

XYZ
===
* archetypes vs. dexterity
  - dexterity & multilinguality?
        -> not supported yet (plone.multilinguality is in progress)
  - dexterity & folderishtypes?
  - dexterity does not support image scaling for now
  -> using archetypes for now.
* yafowil integration?

FUNKTIONALITÄTEN
================
OK * bannerverwaltung
OK * social bookmarks
OK * rss feed integration von CBA und freie-radios.net

theming
-------
OK * deliverance / xdv integration
OK * rules file
OK * theme file

now playing
-----------
OK * kommunikationsprotokoll
* js/zope3 view client
* server

* unmoderiertes musikprogramm: songtitel <- rivendell
* live/vorproduziert: sendungsname <- rivendell/programmverwaltung

kommentarfunktion
-----------------
NO * plone.app.discussion integration
or
OK * collective.disqus integration

kalender ansichten
------------------
* zettwerk.fullcalendar
* integration der programmverwaltungsinhalte in plone?

multilingualität
----------------
OK * Products.LinugaPlone integation

audio/video integration
-----------------------
* collective.flowplayer

gallery
-------
* collective.js.slimbox2
OK * collective.gallery

solr suche
----------
OK * solr integration
* integration mit programmverwaltung

tagcloud
--------
* tagcloud itself
* integration mit solr


