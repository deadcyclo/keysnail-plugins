=======
 About
=======

This plugin allows you to interact with pinboard.in. You can bookmark the current page, store the current page as a read later bookmark and store your current tabset. In addition you get shortcuts to access your unread bookmarks, all of your bookmarks and your stored tabsets.

=========
 Install
=========

This is a plugin for the firefox addon `keysnail <https://github.com/mooz/keysnail>`_. Without firefox and keysnail, this plugin is useless.

Directly from github
====================

+ Klikk on `pinboard.ks.js <https://github.com/deadcyclo/keysnail-plugins/blob/master/pinboard/pinboard.ks.js>`_ above.
+ Right click on the *Raw* button and select *Install this plugin*

Manually
========

+ Download `pinboard.ks.js <https://raw.github.com/deadcyclo/keysnail-plugins/master/pinboard/pinboard.ks.js>`_ and put it in your keysnail plugin directory
+ Reload keysnail through it's menu or restart firefox

=====
 Use
=====

Paste code below to your .keysnail.js file.

.. code:: javascript

  key.setGlobalKey(['C-d', 'd'], function (ev, arg) {
    ext.exec("pinboard-save", arg, ev);
  }, 'Save to pinboard', true);

  key.setGlobalKey(['C-d', 'C-d'], function (ev, arg) {
    ext.exec("pinboard-save-read-later", arg, ev);
  }, 'Save to pinboard as read later', true);

  key.setGlobalKey(['C-d', 't'], function (ev, arg) {
    ext.exec("pinboard-save-tab-set", arg, ev);
  }, 'Save current tab set to pinboard', true);

  key.setGlobalKey(['C-d', 'C-t'], function (ev, arg) {
    ext.exec("pinboard-view-tab-sets", arg, ev);
  }, 'View tabsets on pinboard in new tab', true);

  key.setGlobalKey(['C-d', 'a'], function (ev, arg) {
    ext.exec("pinboard-view-all", arg, ev);
  }, 'View own bookmarks on pinboard in new tab', true);

  key.setGlobalKey(['C-d', 'r'], function (ev, arg) {
    ext.exec("pinboard-view-unread", arg, ev);
  }, 'View unread bookmarks on pinboard in new tab', true);


In this example you get the following keybindings:

========  =============================================================
Shortcut  Action
========  =============================================================
C-d d     Bookmark current page
C-d C-d   Bookmark current page as read later
C-d t     Save current tab set to pinboard
C-d C-t   View your saved tab sets on pinboard in a new tab
C-d a     View all your pinboard bookmarks in a new tab
C-d r     View your bookmarks marked as unread on pinboard in a new tab
========  =============================================================

=========
 License
=========

Copyright 2013 Brendan Johan Lee

This file is part of keysnail pinboard plugin.

keysnail pinboard plugin is free software: you can redistribute
it and/or modify it under the terms of the GNU General Public
License as published by the Free Software Foundation, either
version 3 of the License, or (at your option) any later
version.

keysnail pinboar plugin is distributed in the hope that it will
be useful, but WITHOUT ANY WARRANTY; without even the implied
warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR
PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public
License along with Foobar. If not, see
`http://www.gnu.org/licenses/ <http://www.gnu.org/licenses/>`_.
