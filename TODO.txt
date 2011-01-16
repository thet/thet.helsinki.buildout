===========================
Radio Helsinki Website TODO
===========================

content types
=============
additional
----------
* project
* teaser

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
  - display all subfolders with galleryview enabled
  - searchpath: portal_root, context

* RSS freieradios
* RSS cba

* social bookmarks
  + bookmarks frei wählbar + sortierbar
  + bookmark service frei wählbar
  + eigener bookmark service

* tagcloud / filter

* banner


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
* bannerverwaltung
* social bookmarks
* rss feed integration von CBA und freie-radios.net

theming
-------
* deliverance / xdv integration
* rules file
* theme file

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
* Products.LinugaPlone integation

audio/video integration
-----------------------
* collective.flowplayer

gallery
-------
* collective.js.slimbox2
* collective.gallery

solr suche
----------
OK * solr integration
* integration mit programmverwaltung

tagcloud
--------
* tagcloud itself
* integration mit solr


