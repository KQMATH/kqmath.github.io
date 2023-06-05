# Installation instructions  (QTracker Block)

## Moodle plugins directory

Click on **Install now** within the plugins directory, and then select your site from the list of "My sites"

## Manually
Unzip all the files into a temporary directory.
Rename the **moodle-block_qtracker** folder to **qtracker**, and move it into **moodle/blocks**.
The system administrator should then log in to moodle and click on the **Notifications** link in the Site administration
block.

### From git repo
Instead of downloading the zip file, you can clone the git repo.  Such a working copy of the repo is easier to upgrade than the zip file.  The directory must be renamed and moved as above, and the administrator must log into moodle and click **Notifications** to have moodle upgrade the database.

#### Branches

- master - Stable branch, usually identical to the most recent release.
- develop - The bleeding edge. It is likely to be working, since experiemental development is made on separate branches.

## Requirements
Requires [QTracker](https://github.com/KQMATH/moodle-local_qtracker) and a supported activity module.

# Uninstalling
Delete the module from the **blocks** plugin list in the admin section.
