# Reports installation instructions
## Moodle plugins directory
Click on **Install now** within the [Moodle plugins directory](https://moodle.org/plugins), and then select your site from the list of "My sites".

## Manually
Unzip all the files into a temporary directory.
Rename the **moodle-capquizreport_reportname** folder to **reportname**, and move it into the **moodle/mod/capquiz/report** folder. Where reportname is the name of the report (in lowercase).

The system administrator should then log in to Moodle and click on the **Notifications** link in the Site administration block.

### From git repo
Instead of downloading the zip file, you can clone the git repo. Such a working copy of the repo is easier to upgrade than the zip file. The directory must be renamed and moved as [above](Reports-installation-instructions#manually), and the administrator must log into Moodle and click **Notifications** to have Moodle upgrade the database.

# Uninstalling
Delete the module from the **CAPQuiz / Reports** module list in the **Plugins overview** admin section.