# mythcal

Copyright 2009-2024 Richard Fearn

## Introduction

mythcal is a simple script that synchronizes your MythTV recording schedule to
a Google calendar.

Leaving my MythTV server on 24/7 wastes electricity, but I don't want to forget
to turn it on to record programmes. I wrote this to make it easy to keep track
of upcoming recordings.

## Upgrading from previous versions

Earlier versions of mythcal required you to create a calendar manually, and put
the calendar's ID into a `mythcal.conf` configuration file. This is no longer
necessary. mythcal now requires fewer permissions (it no longer requires full
access to all of your calendars), and it creates its own calendar for MythTV
programmes.

If you are upgrading from an earlier version of mythcal, the quickest way to
migrate is to do the following:

1. Visit [Google Account Security](https://myaccount.google.com/security) and
   remove access for mythcal.

2. Delete `mythcal.conf`. This will contain the ID of a calendar that mythcal
   previously used, but will no longer be able to access (since you created it
   manually).

3. (Optional) Delete the old MythTV calendar from your Google account; mythcal
   will no longer update this.

4. Follow the "Getting started" instructions below, starting at step 3 (Google
   account access).

## Getting started

1. Create a new directory somewhere on your MythTV server and copy the script
   (`mythcal`) into the directory.

2. Install the required packages:

    * MythTV Python bindings (`"libmyth-python"` for Ubuntu; `"python3-MythTV"`
      from RPM Fusion free for Fedora).

    * pytz (`"python3-tz"` for Ubuntu; `"python3-pytz"` for Fedora).

    * Google APIs Client Library for Python (`"python3-googleapi"` for Ubuntu;
      `"python3-google-api-client"` for Fedora).

3. Give mythcal permission to access your Google account. Run `mythcal --auth`
   and follow the instructions.

4. Run mythcal manually with the `--dry-run` or `-n` option. (The first time you
   run this, a new calendar will be created for MythTV programmes.) This will
   tell you what's going to be changed in your calendar.

5. If everything looks good, set up a cron job which will execute mythcal as
   often as you like. The command being run should look something like this:

   `cd /path/to/mythcal/directory && ./mythcal`

## Acknowledgements

Thanks to Michael T. Dean and Raymond Wagner for pointing me in the direction
of the MythTV Python bindings.
