mythcal is a simple script that synchronizes your MythTV recording schedule to a Google calendar.

Leaving my MythTV server on 24/7 wastes electricity, but I don't want to forget to turn it on to record programmes. I wrote this to make it easy to keep track of upcoming recordings.


---


**Update 2014-12-23**
  * **Calendar v3 API**
    * mythcal has been updated to use the Calendar v3 API. Please try version [0.27.0](http://code.google.com/p/mythcal/source/browse/?name=0.27.0). I'd be interested to hear from anyone who encounters time zone problems - where the actual recording times and the start/end times of the calendar entries that mythcal creates don't match.
  * **CHANGES file**
    * There is now a CHANGES file in the source tree that describes any changes in new versions.

---


**Update 2012-06-05**
  * **Git migration**
    * Source code has been migrated from Subversion to Git.
    * The [0.24 branch](http://code.google.com/p/mythcal/source/browse/?name=0.24) is for MythTV 0.24 installations. The latest version is [0.24.1](http://code.google.com/p/mythcal/source/browse/?name=0.24.1).
    * The [master branch](http://code.google.com/p/mythcal/source/browse/?name=master) is for MythTV 0.25 installations. The latest version is [0.25.0](http://code.google.com/p/mythcal/source/browse/?name=0.25.0).
    * 0.24.1 and 0.25.0 are identical.
  * **Wiki removal**
    * The wiki has been deleted. There were only a couple of documentation links in it; those links are [now in the README](http://code.google.com/p/mythcal/source/browse/README?name=0.24.1#81).