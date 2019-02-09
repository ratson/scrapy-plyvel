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

If you encountered the following error::

    Failed to build plyvel

        plyvel/_plyvel.cpp:589:10: fatal error: 'leveldb/db.h' file not found
        #include "leveldb/db.h"
                ^~~~~~~~~~~~~~
        1 error generated.
        error: command 'clang' failed with exit status 1

Try the following install comamnd::

    env CFLAGS="-mmacosx-version-min=10.14 -stdlib=libc++ -I/usr/local/Cellar/leveldb/1.20_2/include/ -L/usr/local/lib" pip install plyvel


Usage
======

In settings.py, for example::

    HTTPCACHE_ENABLED = True
    HTTPCACHE_STORAGE = 'scrapy_plyvel.httpcache.PlyvelCacheStorage'
