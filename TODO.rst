===========================
Radio Helsinki Website TODO
===========================

deployment
==========
* import portlets.xml, reorder right column at /news, /info/mitmachen,
  /info/unterstutzen
* check disqus urls and settings
OK * delete all topics, let them be created by setup_content_structure GS step.
OK * navigation-main, navigation-projekte portlet names. include top für
  navigation-projekte ausschalten
OK * content icons css based
* catalog clear and rebuild
OK * uninstall linuga plone

TODO fin
========

high
----
Ok * now playing
* solr django/plone integration
* https login

* scrolling text for now playing
* weekview display


mid
---
OK * nowplaying calendar widget
OK * facebook portlet
OK * remove LinguaPlone and language viewlet - not needed ATM
OK * content type filters, contextually allowed content types
OK * adapt collective.folderishtraverse - bad usability in admin mode
OK    * projekte: kein hinzüfügen menü?
NO * navigation: new portlet with support for displaying default items
OK * topic/news reverse order
OK * folder summary views: layout customization
OK * project nav: alphabetical? in order of start-date? grouped by year?
OK * programmverwaltungslink unter /programm verlinkt nicht.
* metamenu active states
OK * find a place to put teasers in.
* configure c.gallery to use correct sizes
OK * configure all content types, if they don't look appropriate.
OK * zettwerk.fullcalendar
* collective.flowplayer
OK * display gernam html titles for program area
OK * folderish_summary_view ohne bilder -> <img> tag+eigenartiges layout
OK * disqus integration
OK * styling

projekte
........
- An Hannes: cool wäre eine Unterscheidung zwischen Themenschwerpunkten,
  Festvalbegleitung, Eigene Projekte sowie die Ordnung nach Jahreszahlen.
  Schön wäre es, wenn man das dann danach sortieren könnte.



low
---
* suche: suchseite soll mit wildcards funktionieren.
* livestream: collective.nakedviews -> views without plone context
* teaser edit screen importance displays only number
* collective.folderishtypes: let CT derive all other interfaces too... currently they are overwritten.
* backport changes to folder_listing and folder_summary_view to plone



BUGS
====

zettwerk.fullcalendar view -> html entities are escaped again. problem with
deliverance?

2011-05-09 17:54:51 ERROR portlets Error while rendering <plone.app.portlets.manager.ColumnPortletManagerRenderer object at 0xd2747ec>
Traceback (most recent call last):
  File "/home/thet/.buildout/eggs/plone.app.portlets-2.0.3-py2.6.egg/plone/app/portlets/manager.py", line 59, in safe_render
    return portlet_renderer.render()
  File "/home/thet/.buildout/eggs/Zope2-2.12.17-py2.6-linux-i686.egg/Products/Five/browser/pagetemplatefile.py", line 126, in __call__
    return self.im_func(im_self, *args, **kw)
  File "/home/thet/.buildout/eggs/Zope2-2.12.17-py2.6-linux-i686.egg/Products/Five/browser/pagetemplatefile.py", line 60, in __call__
    sourceAnnotations=getattr(debug_flags, 'sourceAnnotations', 0),
  File "/home/thet/.buildout/eggs/zope.pagetemplate-3.5.2-py2.6.egg/zope/pagetemplate/pagetemplate.py", line 113, in pt_render
    strictinsert=0, sourceAnnotations=sourceAnnotations)()
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 271, in __call__
    self.interpret(self.program)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 531, in do_optTag_tal
    self.no_tag(stuff[-2], stuff[-1])
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 513, in no_tag
    self.interpret(program)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 852, in do_condition
    self.interpret(block)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 821, in do_loop_tal
    self.interpret(block)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 533, in do_optTag_tal
    self.do_optTag(stuff)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 518, in do_optTag
    return self.no_tag(start, program)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 513, in no_tag
    self.interpret(program)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 531, in do_optTag_tal
    self.no_tag(stuff[-2], stuff[-1])
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 513, in no_tag
    self.interpret(program)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 343, in interpret
    handlers[opcode](self, args)
  File "/home/thet/.buildout/eggs/zope.tal-3.5.2-py2.6.egg/zope/tal/talinterpreter.py", line 742, in do_insertStructure_tal
    structure = self.engine.evaluateStructure(expr)
  File "/home/thet/.buildout/eggs/Zope2-2.12.17-py2.6-linux-i686.egg/Products/PageTemplates/Expressions.py", line 220, in evaluateStructure
    text = super(ZopeContext, self).evaluateStructure(expr)
  File "/home/thet/.buildout/eggs/zope.tales-3.4.0-py2.6.egg/zope/tales/tales.py", line 696, in evaluate
    return expression(self)
  File "/home/thet/.buildout/eggs/zope.tales-3.4.0-py2.6.egg/zope/tales/pythonexpr.py", line 59, in __call__
    return eval(self._code, vars)
  File "<string>", line 1, in <module>
  File "/home/thet/.buildout/eggs/plone.app.blob-1.4-py2.6.egg/plone/app/blob/mixins.py", line 78, in tag
    return field.tag(self, **kwargs)
  File "/home/thet/.buildout/eggs/Products.Archetypes-1.6.6-py2.6.egg/Products/Archetypes/Field.py", line 2598, in tag
    'height="%(height)s" width="%(width)s"' % values
UnicodeDecodeError: 'ascii' codec can't decode byte 0xc3 in position 26: ordinal not in range(128)
2011-05-09 17:54:51 ERROR Zope.SiteErrorLog 1304956491.780.398140633129 http://localhost:8880/info/traverse_view
Traceback (innermost last):
  Module plone.app.portlets.manager, line 59, in safe_render
  Module Products.Five.browser.pagetemplatefile, line 126, in __call__
  Module Products.Five.browser.pagetemplatefile, line 60, in __call__
  Module zope.pagetemplate.pagetemplate, line 113, in pt_render
  Module zope.tal.talinterpreter, line 271, in __call__
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 531, in do_optTag_tal
  Module zope.tal.talinterpreter, line 513, in no_tag
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 852, in do_condition
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 821, in do_loop_tal
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 533, in do_optTag_tal
  Module zope.tal.talinterpreter, line 518, in do_optTag
  Module zope.tal.talinterpreter, line 513, in no_tag
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 531, in do_optTag_tal
  Module zope.tal.talinterpreter, line 513, in no_tag
  Module zope.tal.talinterpreter, line 343, in interpret
  Module zope.tal.talinterpreter, line 742, in do_insertStructure_tal
  Module Products.PageTemplates.Expressions, line 220, in evaluateStructure
  Module zope.tales.tales, line 696, in evaluate
   - URL: /home/thet/dev/helsinki-web/thet.helsinki.buildout/src/collective.gallery/collective/gallery/portlets/show_galleries.pt
   - Line 24, Column 12
   - Expression: <PythonExpr (picture.tag(scale=view.image_scale))>
   - Names:
      {'args': (),
       'container': <ATFolder at /radio-helsinki/helsinki/info>,
       'context': <ATFolder at /radio-helsinki/helsinki/info>,
       'default': <object object at 0xb77d6520>,
       'here': <ATFolder at /radio-helsinki/helsinki/info>,
       'loop': {},
       'nothing': None,
       'options': {},
       'repeat': <Products.PageTemplates.Expressions.SafeMapping object at 0xd26f464>,
       'request': <HTTPRequest, URL=http://localhost:8880/info/traverse_view>,
       'root': <Application at >,
       'template': <Products.Five.browser.pagetemplatefile.ViewPageTemplateFile object at 0xa80c1ac>,
       'traverse_subpath': [],
       'user': <PropertiedUser 'admin'>,
       'view': <collective.gallery.portlets.show_galleries.Renderer object at 0xd1957cc>,
       'views': <Products.Five.browser.pagetemplatefile.ViewMapper object at 0xd276fac>}
  Module zope.tales.pythonexpr, line 59, in __call__
   - __traceback_info__: (picture.tag(scale=view.image_scale))
  Module <string>, line 1, in <module>
  Module plone.app.blob.mixins, line 78, in tag
  Module Products.Archetypes.Field, line 2598, in tag
UnicodeDecodeError: 'ascii' codec can't decode byte 0xc3 in position 26: ordinal not in range(128)




content structure
-----------------
- impressum
- kontakt aus metamenu weg
--> check it for live site too!




ie html5 javascript not needed ATM
----------------------------------
  <!--[if lt IE 9]>
  <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
  <![endif]-->


protokoll 29.03.11
==================

Homepage
========
Inhalte müssen eingetragen werden!!!
- Leo nachfragen, wann allgemeiner Text kommt. Robin macht.
- Gremien: in "Arbeitsbereiche" umbenennen: Moke
- Unterstützen: Robin
- Presse: Hannes bitte Logos reinstellen und in "Presse" in "Logo" umbenennen. Danke!
- Startseite: Hannes und Nene schreiben Eröffnungstext.
- Projekte: 
alte Projekte: Radiodialoge (Angela), MONA (Moke), Nicaragua (Walt), Tagungen (Gudrun), Sex (Robin), Tod (Robin), Annenviertel (Mak), Afrikaschwerpunkt (Robin), 16Tage (Robin), 8.März (Robin).
aktuelle Projekte: WWA (Robin)
geplante Projekte: 4elements (Gudrun informiert Imre), elevate (Mak), Lendwirbel (Robin Sagt Günther), Chiala (Gudrun)

An Hannes: cool wäre eine Unterscheidung zwischen Themenschwerpunkten, Festvalbegleitung, Eigene Projekte sowie die Ordnung nach Jahreszahlen. Schön wäre es, wenn man das dann danach sortieren könnte.


WHAT NEXT?
==========

OK * footer

OK * content icons css based

OK impressum
OK kontakt aus metamenu weg
--> check it for live site too!

deliverance fixes
OK 1) the policy for when subrequests to Deliverance's inner URL-space should be sent back out to Deliverance
OK 2) the headers sent in those subrequests
OK 3) the DeliveranceMiddleware instance used in deliverance-proxy

OK * public.css removed by deliverance (disable grouping), so that backend is
  still styled

OK * teaser und projekt - selbes icon - ändern
OK * ical/vcal bei projekten rausnehmen
* suche: suchseite soll mit wildcards funktionieren.
OK * benutzer: wegschalten
OK * benutzer: keine rechte projekte anzulegen?
OK * kalenderblatt - not styled
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
OK * users, groups, rights and config

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
NO * collective.js.slimbox2
OK * collective.gallery

solr suche
----------
OK * solr integration
* integration mit programmverwaltung

tagcloud
--------
NO * tagcloud itself
NO * integration mit solr


