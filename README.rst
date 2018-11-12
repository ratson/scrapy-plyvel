==============
Scrapy-Plyvel
==============

Requirements
============

* Python 3.7+
* Works on Linux, Windows, Mac OSX, BSD

Install
=======

The quick way::

    pip install scrapy-plyvel

OR copy this middleware to your scrapy project.

Usage
======

In settings.py, for example::

    HTTPCACHE_ENABLED = True
    HTTPCACHE_STORAGE = 'scrapy_plyvel.httpcache.PlyvelCacheStorage'
