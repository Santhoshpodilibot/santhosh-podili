
..
    Make sure to apply any changes to this file to README_RAW.rst as well!

.. image:: https://github.com/python-telegram-bot/logos/blob/master/logo-text/png/ptb-logo-text_768.png?raw=true
   :align: center
   :target: https://python-telegram-bot.org
   :alt: python-telegram-bot Logo

We have made you a wrapper you can't refuse

We have a vibrant community of developers helping each other in our `Telegram group <https://telegram.me/pythontelegrambotgroup>`_. Join us!

*Stay tuned for library updates and new releases on our* `Telegram Channel <https://telegram.me/pythontelegrambotchannel>`_.

.. image:: https://img.shields.io/pypi/v/python-telegram-bot.svg
   :target: https://pypi.org/project/python-telegram-bot/
   :alt: PyPi Package Version

.. image:: https://img.shields.io/pypi/pyversions/python-telegram-bot.svg
   :target: https://pypi.org/project/python-telegram-bot/
   :alt: Supported Python versions

.. image:: https://img.shields.io/badge/Bot%20API-5.6-blue?logo=telegram
   :target: https://core.telegram.org/bots/api-changelog
   :alt: Supported Bot API versions

.. image:: https://img.shields.io/pypi/dm/python-telegram-bot
   :target: https://pypistats.org/packages/python-telegram-bot
   :alt: PyPi Package Monthly Download

.. image:: https://readthedocs.org/projects/python-telegram-bot/badge/?version=stable
   :target: https://python-telegram-bot.readthedocs.io/en/stable/?badge=stable
   :alt: Documentation Status

.. image:: https://img.shields.io/pypi/l/python-telegram-bot.svg
   :target: https://www.gnu.org/licenses/lgpl-3.0.html
   :alt: LGPLv3 License

.. image:: https://github.com/python-telegram-bot/python-telegram-bot/workflows/GitHub%20Actions/badge.svg
   :target: https://github.com/python-telegram-bot/python-telegram-bot/
   :alt: Github Actions workflow

.. image:: https://codecov.io/gh/python-telegram-bot/python-telegram-bot/branch/master/graph/badge.svg
   :target: https://codecov.io/gh/python-telegram-bot/python-telegram-bot
   :alt: Code coverage

.. image:: http://isitmaintained.com/badge/resolution/python-telegram-bot/python-telegram-bot.svg
   :target: http://isitmaintained.com/project/python-telegram-bot/python-telegram-bot
   :alt: Median time to resolve an issue

.. image:: https://api.codacy.com/project/badge/Grade/99d901eaa09b44b4819aec05c330c968
   :target: https://www.codacy.com/app/python-telegram-bot/python-telegram-bot?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=python-telegram-bot/python-telegram-bot&amp;utm_campaign=Badge_Grade
   :alt: Code quality: Codacy

.. image:: https://deepsource.io/gh/python-telegram-bot/python-telegram-bot.svg/?label=active+issues
   :target: https://deepsource.io/gh/python-telegram-bot/python-telegram-bot/?ref=repository-badge
   :alt: Code quality: DeepSource

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
   :target: https://github.com/Santhoshpodilibot/santhosh-podili/tree/patch-5

.. image:: https://img.shields.io/badge/Telegram-Group-blue.svg?logo=telegram
   :target: https://t.me/newsstreamer
   :alt: Telegram Group

=================
Table of contents
=================

- `Introduction`_

- `Telegram API support`_

- `Installing`_

- `Getting started`_

  #. `Learning by example`_

  #. `Logging`_

  #. `Documentation`_

- `Getting help`_

- `Contributing`_

- `License`_

============
Introduction
============

This library provides a pure Python interface for the
`Telegram Bot API <https://core.telegram.org/bots/api>`_.
It's compatible with Python versions 3.6.8+. PTB might also work on `PyPy <http://pypy.org/>`_, though there have been a lot of issues before. Hence, PyPy is not officially supported.

In addition to the pure API implementation, this library features a number of high-level classes to
make the development of bots easy and straightforward. These classes are contained in the
``telegram.ext`` submodule.

A pure API implementation *without* ``telegram.ext`` is available as the standalone package ``python-telegram-bot-raw``.  `See here for details. <https://github.com/python-telegram-bot/python-telegram-bot/blob/master/README_RAW.rst>`_

----
Note
----

Installing both ``python-telegram-bot`` and ``python-telegram-bot-raw`` in conjunction will result in undesired side-effects, so only install *one* of both.

====================
Telegram API support
====================

All types and methods of the Telegram Bot API **5.6** are supported.

==========
Installing
==========

You can install or upgrade python-telegram-bot with:

.. code:: shell

    $ pip install python-telegram-bot --upgrade

Or you can install from source with:

.. code:: shell

    $ git clone https://github.com/python-telegram-bot/python-telegram-bot --recursive
    $ cd python-telegram-bot
    $ python setup.py install
    
In case you have a previously cloned local repository already, you should initialize the added urllib3 submodule before installing with:

.. code:: shell

    $ git submodule update --init --recursive

---------------------
Optional Dependencies
---------------------

PTB can be installed with optional dependencies:

* ``pip install python-telegram-bot[passport]`` installs the `cryptography <https://cryptography.io>`_ library. Use this, if you want to use Telegram Passport related functionality.
* ``pip install python-telegram-bot[ujson]`` installs the `ujson <https://pypi.org/project/ujson/>`_ library. It will then be used for JSON de- & encoding, which can bring speed up compared to the standard `json <https://docs.python.org/3/library/json.html>`_ library.
* ``pip install python-telegram-bot[socks]`` installs the `PySocks <https://pypi.org/project/PySocks/>`_ library. Use this, if you want to work behind a Socks5 server.

===============
Getting started
===============

Our Wiki contains a lot of resources to get you started with ``python-telegram-bot``:

- `Introduction to the API <https://github.com/python-telegram-bot/python-telegram-bot/wiki/Introduction-to-the-API>`_
- Tutorial: `Your first Bot <https://github.com/python-telegram-bot/python-telegram-bot/wiki/Extensions-%E2%80%93-Your-first-Bot>`_

Other references:

- `Telegram API documentation <https://core.telegram.org/bots/api>`_
- `python-telegram-bot documentation <https://python-telegram-bot.readthedocs.io/>`_

-------------------
Learning by example
-------------------

We believe that the best way to learn this package is by example. Here
are some examples for you to review. Even if it is not your approach for learning, please take a
look at ``echobot.py``, it is the de facto base for most of the bots out there. Best of all,
the code for these examples are released to the public domain, so you can start by grabbing the
code and building on top of it.

Visit `this page <https://github.com/python-telegram-bot/python-telegram-bot/blob/master/examples/README.md>`_ to discover the official examples or look at the examples on the `wiki <https://github.com/python-telegram-bot/python-telegram-bot/wiki/Examples>`_ to see other bots the community has built.

-------
Logging
-------

This library uses the ``logging`` module. To set up logging to standard output, put:

.. code:: python

    import logging
    logging.basicConfig(level=logging.DEBUG,
                        format='%(asctime)s - %(name)s - %(levelname)s - %(message)s')

at the beginning of your script.

You can also use logs in your application by calling ``logging.getLogger()`` and setting the log level you want:

.. code:: python

    logger = logging.getLogger()
    logger.setLevel(logging.INFO)

If you want DEBUG logs instead:

.. code:: python

    logger.setLevel(logging.DEBUG)


=============
Documentation
=============

``python-telegram-bot``'s documentation lives at `readthedocs.io <https://python-telegram-bot.readthedocs.io/>`_.

============
Getting help
============

You can get help in several ways:

1. We have a vibrant community of developers helping each other in our `Telegram group <https://telegram.me/pythontelegrambotgroup>`_. Join us!

3. Our `Wiki pages <https://github.com/python-telegram-bot/python-telegram-bot/wiki/>`_ offer a growing amount of resources.

4. You can even ask for help on Stack Overflow using the `python-telegram-bot tag <https://stackoverflow.com/questions/tagged/python-telegram-bot>`_.


============
Contributing
============

Contributions of all sizes are welcome. Please review our `contribution guidelines <https://github.com/python-telegram-bot/python-telegram-bot/blob/master/.github/CONTRIBUTING.rst>`_ to get started. You can also help by `reporting bugs <https://github.com/python-telegram-bot/python-telegram-bot/issues/new>`_.

========
Donating
========
Occasionally we are asked if we accept donations to support the development. While we appreciate the thought, maintaining PTB is our hobby and we have almost no running costs for it. We therefore have nothing set up to accept donations. If you still want to donate, we kindly ask you to donate to another open source project/initiative of your choice instead.

=======
License
=======

You may copy, distribute and modify the software provided that modifications are described and licensed for free under `LGPL-3 <https://www.gnu.org/licenses/lgpl-3.0.html>`_. Derivatives works (including modifications or anything statically linked to the library) can only be redistributed under LGPL-3, but applications that use the library don't have to be.






# santhosh-podili
Hi


# SANTHOSHPODILI
Telegram bot to stream videos in telegram voicechat for both groups and channels. Supports live streams, YouTube videos and telegram media. With record stream support, Schedule streams, and many more.

## Config Vars:
### Mandatory Vars
1. `API_ID` : Get From [my.telegram.org](https://my.telegram.org/)
2. `API_HASH` : Get from [my.telegram.org](https://my.telegram.org)
3. `BOT_TOKEN` : [@Botfather](https://telegram.dog/BotFather)
4. `SESSION_STRING` : Generate From here [![GenerateStringName](https://img.shields.io/badge/repl.it-generateStringName-yellowgreen)](https://replit.com/@ALBINPRAVEEN1/getStringName)
5. `CHAT` : ID of Channel/Group where the bot plays Music.
6. `OWNER_ID`  : [@MissRose_bot]
7. `BOT_PIC` : https://te.legra.ph/file/509686aa88a027bffe2b3.jpg  Get from [@vTelegraphBot]
## Recommended Optional Vars

1. `DATABASE_URI`: MongoDB database Url, get from [mongodb](https://cloud.mongodb.com). This is an optional var, but it is recomonded to use this to experiance the full features.
2. `HEROKU_API_KEY`: Your heroku api key. Get one from [here](https://dashboard.heroku.com/account/applications/authorizations/new)
3. `HEROKU_APP_NAME`: Your heroku apps name.
4. `FILTERS`: Filter the search for channel play. Channel play means you can play all the files in a purticular channel using /cplay command. Current filters are `video document` . For searching audio files use `video document audio` . for video only search , use `video` and so on.

### Optional Vars
1. `LOG_GROUP` : Group to send Playlist, if CHAT is a Group()
2. `ADMINS` : ID of users who can use admin commands.
3. `STARTUP_STREAM` : This will be streamed on startups and restarts of bot. You can use either any STREAM_URL or a direct link of any video or a Youtube Live link. You can also use YouTube Playlist.Find a Telegram Link for your playlist from [PlayList Dumb](https://telegram.dog/DumpPlaylist) or get a PlayList from [ALBINPRAVEEN](https://telegram.dog/i_am_albin_ptaveen).
4. `REPLY_MESSAGE` : A reply to those who message the USER account in PM. Leave it blank if you do not need this feature. (Configurable through bot if mongodb added.)
5. `ADMIN_ONLY` : Pass `True` If you want to make /play command only for admins of `CHAT`. By default /play is available for all.(Configurable through bot if mongodb added.)
6. `DATABASE_NAME`: Database name for your mongodb database.
7. `SHUFFLE` : Make it `False` if you dont want to shuffle playlists. (Configurable through bot if mongodb added.)
8. `EDIT_TITLE` : Make it `False` if you do not want the bot to edit video chat title according to playing song. (Configurable through bot if mongodb added.)
9. `RECORDING_DUMP` : A Channel ID with the USER account as admin, to dump video chat recordings.
10. `RECORDING_TITLE`: A custom title for your videochat recordings.
11. `TIME_ZONE` : Time Zone of your country, by default IST
12. `IS_VIDEO_RECORD` : Make it `False` if you do not want to record video, and only audio will be recorded.(Configurable through bot if mongodb added.)
13. `IS_LOOP` ; Make it `False` if you do not want 24 / 7 Video Chat. (Configurable through bot if mongodb added.)
14. `IS_VIDEO` : Make it `False` if you want to use the player as a musicplayer without video. (Configurable through bot if mongodb added.)
15. `PORTRAIT`: Make it `True` if you want the video recording in portrait mode. (Configurable through bot if mongodb added.)
16. `DELAY` : Choose the time limit for commands deletion. 10 sec by default.
18. `QUALITY` : Customize the quality of video chat, use one of `high`, `medium`, `low` . 
19. `BITRATE` : Bitrate of audio (Not recommended to change).
20. `FPS` : Fps of video to be played (Not recommended to change.)



## Requirements
- Python 3.8 or Higher.
- [FFMpeg](https://www.ffmpeg.org/).



## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://git.heroku.com/santhupodilivc.git

## Deploy to VPS

```sh
git clone  https://github.com/santhu874/AlbyVideoPlayer1.git
cd AlbyVideoPlayer
pip3 install -r requirements.txt
# <Create Variables appropriately (.env [optional])>
py
```

## Features

- Playlist, queue.
- Zero downtime in playing.
- Supports Video Recording.
- Supports Scheduling voicechats.
- Cool UI for controling the player.
- Customizabe to audio or video.
- Custom quality for video chats.
- Supports Play from Youtube Playlist.
- Change VoiceChat title to current playing song name.
- Supports Live streaming from youtube
- Play from telegram file supported.
- Starts Radio after if no songs in playlist.
- Automatic restart even if heroku restarts. (Configurable)
- Support exporting and importing playlist.

