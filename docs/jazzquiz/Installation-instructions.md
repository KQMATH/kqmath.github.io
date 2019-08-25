# Installation instructions
## Moodle plugins directory
Click on **Install now** within the plugins directory, and then select your site from the list of "My sites"

## Manually
Unzip all the files into a temporary directory.
Rename the **moodle-mod_jazzquiz** folder to **jazzquiz**, and move it into **moodle/mod**.
The system administrator should then log in to moodle and click on the **Notifications** link in the Site administration
block.
### From git repo

Instead of downloading the zip file, you can clone the git repo.  Such a working copy of the repo is easier to upgrade than the zip file.  The directory must be renamed and moved as above, and the administrator must log into moodle and click **Notifications** to have moodle upgrade the database.

#### Branches

- vX.X - Release branch.  These branches are only updated with bugfixes to produce minor revisions.
- master - Stable branch, usually identical to the most recent release.
- develop - The bleeding edge. It is likely to be working, since experiemental development is made on separate branches.

# Configuration
If you are using mathematics, make sure MathJax is enabled.
  * Site management → Filter → Manage filters → MathJax: Choose Contents and Headings in the drop down menu.

# Uninstalling
Delete the module from the **Activities** module list in the admin section.