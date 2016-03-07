Moodle Meta Link Group and Grouping Synchronization
===================================================

Requirements
------------
- Moodle 2.7 (build 2014051200) or later.
- Meta-course enrolment (build 2014051200 or later).

Installation
------------
Copy the metagroups folder into your Moodle /local directory and visit your Admin Notification page to complete the installation.

Usage
-----
After installation, or when creating new meta-course enrolment instances, you may need to synchronize existing groups. To do this
run the cli/sync.php script (use the --help switch for further instructions on usage) or enable Meta-course groups and groupings 
synchronization scheduled task.

Any future amendments to groups (add, update and delete) and their membership (add or remove users) in 'child' courses will be automatically
reflected in 'parent' courses that use groups.

Authors
-------
- Paul Holden (pholden@greenhead.ac.uk) 
- Vadim Dvorovenko (Vadimon@mail.ru)
- François Lumineau (flumineau@iae.univ-poitiers.fr)
- Danny Jung (dannyjung90@gmail.com)

Links
-----
- Updates: https://moodle.org/plugins/view.php?plugin=local_metagroups
- Latest code: https://github.com/paulholden/moodle-local_metagroups

Changes
-------
Release 1.4 (build 2016022806):
- Add scheduled tasks for synchronization.
- Synchronize parent courses that use groups or all courses, depending on setting.
- Synchronization of groupings on meta courses, depending on settings. Groupings are syncronized 
on-the-fly. Group to groupings assignments are syncronized on sync task (prior to Moodle 3.1) or
on event trigger (Moodle 3.1 and higher).
- Synchronization of group description and picture.
- Added automatic syncronization on meta enrol instance creation (Moodle 3.0 and higher).

Release 1.3 (build 2014103100):
- CLI script can now synchronize specific courses.
- API & documentation updates.

Release 1.2 (build 2014080500):
- Only synchronize parent courses that use groups.

Release 1.1 (build 2014031300):
- Prevent synchronized group memberships being removed.

Release 1.0 (build 2014021001):
- First release.
