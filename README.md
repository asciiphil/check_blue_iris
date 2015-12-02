check_blue_iris
===============

This is a very simple Nagios plugin that checks on the health of a
[Blue Iris][] video recording server.  It uses Blue Iris's JSON API, which
means you need to have the web server enabled in order to use this plugin.

  [Blue Iris]: http://blueirissoftware.com/


Installation
------------

The plugin requires Python version 2.6 or later on the testing system.  It
shouldn't require anything else.  On the system to be monitored, the web
server must be enabled and accessible (ports opened on the Windows
firewall, etc.).  The plugin should be fairly self-explanatory via its
`--help` option.


Limitations
-----------

The health checking is fairly simplistic: it complains if recording is
globally disabled or if one or more of the configured cameras are offline.
It does not complain if a particular camera happens not to be recording at
the moment, because all of the author's cameras only record when triggered
by motion detection.

If you need additional error criteria, please feel free to contact the
author ([Phil! Gold](mailto:phil_g@pobox.com)) and either describe how
your setup works or send a patch/pull request.
