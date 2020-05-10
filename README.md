# mythcal

Copyright 2009-2020 Richard Fearn

## Introduction

mythcal is a simple script that synchronizes your MythTV recording schedule to
a Google calendar.

Leaving my MythTV server on 24/7 wastes electricity, but I don't want to forget
to turn it on to record programmes. I wrote this to make it easy to keep track
of upcoming recordings.

## Getting started

1. Create a calendar in Google Calendar that will hold your MythTV programmes.
   DO NOT USE YOUR MAIN GOOGLE CALENDAR! YOU MUST CREATE A NEW CALENDAR!
   mythcal synchronises your programmes by deleting everything from the
   calendar, then adding an event for each programme.

2. Create a new directory somewhere on your MythTV server and copy the script
   (`mythcal`) and the template configuration file (`mythcal.conf.template`) into
   the directory.

3. Install the required packages:

    * MythTV Python bindings (`"libmyth-python"` for Ubuntu; `"python3-MythTV"`
      from RPM Fusion free for Fedora).

    * pytz (`"python3-tz"` for Ubuntu; `"python3-pytz"` for Fedora).

    * Google APIs Client Library for Python (`"python3-googleapi"` for Ubuntu;
      `"python3-google-api-client"` for Fedora).

4. Copy the template configuration file, `mythcal.conf.template`, to
   `mythcal.conf`, and add the missing settings. The sections are:

    * `[calendar]` - details about your Google Calendar. To find the `"id"`, go into
      Google Calendar Settings, click the calendar you want to use under
      "Settings for my calendars" on the left-hand side, and look in the
      "Integrate calendar" section. The Calendar ID
      should be displayed: it will look something like
      `"abc123def@group.calendar.google.com"`. Please remember: USE A SEPARATE
      CALENDAR FOR MYTHCAL, or your appointments will be deleted!

5. Give mythcal permission to access your calendar. Run `mythcal --auth` and
   follow the instructions.

6. Run mythcal manually with the `--dry-run` or `-n` option. This will tell you
   what's going to be changed in your Google Calendar. Hopefully it won't tell
   you that your important appointments are going to be deleted, because you'll
   be using a **separate** calendar for mythcal!

7. If everything looks good, set up a cron job which will execute mythcal as
   often as you like. The command being run should look something like this:

   `cd /path/to/mythcal/directory && ./mythcal`

## Acknowledgements

Thanks to Michael T. Dean and Raymond Wagner for pointing me in the direction
of the MythTV Python bindings.
