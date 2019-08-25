# Installation instructions 
## Moodle plugins directory
Click on **Install now** within the plugins directory, and then select your site from the list of "My sites"

## Manually
Unzip all the files into a temporary directory.
Rename the **moodle-mod_capquiz** folder to **capquiz**, and move it into **moodle/mod**.
The system administrator should then log in to moodle and click on the **Notifications** link in the Site administration
block.

### From git repo

Instead of downloading the zip file, you can clone the git repo.  Such a working copy of the repo is easier to upgrade than the zip file.  The directory must be renamed and moved as above, and the administrator must log into moodle and click **Notifications** to have moodle upgrade the database.

#### Branches

- developmnet
- master

**TODO** Add comments.  Add release branches.


## Requirements
Be sure to meet CAPQuiz's [requirements](https://github.com/KQMATH/moodle-mod_capquiz/wiki/Requirements).

# Uninstalling
Delete the module from the **Activities** module list in the admin section.

# Sub-plugins
Each sub-plugin type defines its own installation instruction. One does not need to install the sub-plugin types implementations that ships with CAPQuiz. Although, they can be uninstalled if preferred.

For detailed installation instructions, see:
* [Reports installation instructions](Reports-installation-instructions)