.. SPDX-FileCopyrightText: 2012-2022 Tobias Leupold <tl at stonemx dot de>

   SPDX-License-Identifier: CC-BY-SA-4.0

   The format of this file is inspired by keepachangelog.com, but uses ReStructuredText instead of
   MarkDown. Keep the line length at no more than 100 characters (with the obvious exception of the
   header template below, which needs to be indented by three spaces)

   Here's the header template to be pasted at the top after a new release:

   ====================================================================================================
   [unreleased]
   ====================================================================================================

   Added
   =====

   * for new features.

   Changed
   =======

   * for changes in existing functionality.

   Deprecated
   ==========

   * for soon-to-be removed features.

   Removed
   =======

   * for now removed features.

   Fixed
   =====

   * for any bug fixes.

   Security
   ========

   * in case of vulnerabilities.

====================================================================================================
[unreleased]
====================================================================================================

Added
=====

* for new features.

Changed
=======

* for changes in existing functionality.

Deprecated
==========

* for soon-to-be removed features.

Removed
=======

* for now removed features.

Fixed
=====

* for any bug fixes.

Security
========

* in case of vulnerabilities.

====================================================================================================
gpx2svg 0.2.0 released (05.09.2021)
====================================================================================================

* New: Added true-scale conversion using a WGS84 projection. Big thanks to Hans Busch for
  contributing the respective code!

* Change: The project is now licensed under the terms of the GPLv3 or later. Also switched all
  headers to SPDX license identifiers and added license notes to all files.

* Change: ChangeLog is now a valid RST document

====================================================================================================
gpx2svg 0.1.5 released (22.07.2018)
====================================================================================================

* New: Added a function to join all segments of a GPX file in the (chronologically) given order of
  the GPS data. This can help to create an un-scattered output if the segments don't share points
  at the beginning and end and thus, the default combining algorithm won't work.
  Thanks to Emiel Brommer for the initial patch!

* Change: Updated the ChangeLog to a more meaningful format.

====================================================================================================
gpx2svg 0.1.4 released (04.01.2015)
====================================================================================================

* Improvement: Replaced the function creating a coordinate string for a segment by a generator. Now,
  segments drawing instructions are created step by step instead of assembling a (probably huge)
  single string.

====================================================================================================
gpx2svg 0.1.3 released (09.03.2014)
====================================================================================================

* Bugfix: Changed the shebang line so that gpx2svg now also runs on Mac

* Bugfix: Changed the use of the literal "/dev/stdin" and "/dev/stdout" to sys.stdin and sys.stdout.
  Hopefully, gpx2svg will now also work on Windows (not tested).

* Generally: Overall code cleanup

====================================================================================================
gpx2svg 0.1.2 released (07.11.2013)
====================================================================================================

* Bugfix: Fixed crash when processing GPX files with empty or no path segments.
  Thanks to Fabian Seitz for the bug report!

* Improvement: Added exception handler for non-readable or non-existant files or files with no valid
  GPX data.

====================================================================================================
gpx2svg 0.1.1 released (26.08.2012)
====================================================================================================

* Improvement: Made the internal data structure simpler. Don't store the IDs of the tracks.

* Improvement/Bugfix: Combine path segments before doing the Mercator projection, so that rounding
  errors can't affect the search.

* Improvement: Made the algorithm to search for combinable paths more effective.

* New: Draw circles instead of single points (that will not be shown). Added a command line option
  to drop such single points.

====================================================================================================
gpx2svg 0.1 released (25.08.2012)
====================================================================================================

* New: Initial release
