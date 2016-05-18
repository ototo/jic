JIC - JIRA CLI Client
=====================

MOTIVATION
----------

To provide an engineer-friendly in-terminal interface to Atlassian JIRA.


HISTORICAL BACKGROUND
---------------------

Initially jic was prototyped in Python. That language was selected to
speed up the proof-of-concept development to make it cheaper and speed
up the switch over to a proper implementation in C.

Due to the lack of bandwidth the original author allowed the prototype
to bitrot to a degree when it can't be installed on a fresh modern
system (as of May 2016).

The decision has been made to perform the switch over in the end of May
2016 and start the development of a proper version of jic. The effort is
supported by Linaro <http://www.linaro.org> as one of the primary users
for the tool.


SOURCES
-------

JIC sources are hosted on GitHub at:

    https://github.com/ototo/jic


VERSIONING
----------

The project uses semantic versioning (see http://semver.org/ for
explanation for the approach).


CONTRIBUTING
------------

Please join jic-dev mailing list hosted by Linaro:

    http://lists.linaro.org/mailman/listinfo/jic-dev

Patches are expected to be sent as emails to the mailing list (above).

Bugs and feature requests are tracked on GitHub:

    https://github.com/ototo/jic/issues


AUTHORS
-------

1. Serge Broslavsky <serge.broslavsky@linaro.org>
    The idea, design, core of the tool, maintainership.


LICENSE
-------

This program is free software: you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation, version 2 of the License.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

You should have received a copy of the GNU General Public License along
with this program. If not, see <http://www.gnu.org/licenses/>.

Documentation and all the artwork or this program is distributed under
Creative Commons Attribution-ShareAlike (CC BY-SA) license (unless it's
stated otherwise for a particular product). You should have received a
copy of that license. If not, see <http://creativecommons.org/licenses/>.
