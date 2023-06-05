# Installation instructions  (QTracker Block)

To use QTracker, you have to install both the block plugin and the local plugin.
Both are installed in the same way.

## Moodle plugins directory

Click on **Install now** within the plugins directory, and then select your site from the list of "My sites"

## Manually from the PKzip archive

Unzip all the files into a temporary directory.

- the **moodle-block_qtracker** directory should be moved into **moodle/blocks** and renamed to **qtracker**.
- the **moodle-local_qtracker** directory should be moved into **moodle/local** and renamed to **qtracker**.

The system administrator should then log in to moodle and click on the **Notifications** link in the Site administration
block.

## From git repo

Instead of downloading the zip file, you can clone the git repo.
Such a working copy of the repo is easier to upgrade than the zip file.
The directories must be moved and renamed as above,
and the administrator must log into moodle and click **Notifications** to have moodle upgrade the database.

### Branches

Both plugin repos use the same naming conventions; there are two ranches to choose between.

- master - Stable branch, usually identical to the most recent release.
- develop - The bleeding edge. It is likely to be working, since experiemental development is made on separate branches.

# Uninstalling

Delete the module from both the **local** and **blocks** plugin lists in the admin section.
