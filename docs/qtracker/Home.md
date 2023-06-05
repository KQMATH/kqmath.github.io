# QTracker

Question Tracker - Issue Tracker for Question Development

QTracker provides a system to record and manage reported problems
with moodle questions.

1. Students get a user interface where they can report problems, be that
   functional errors in the question or feedback which is uninstructive.
2. Teachers get a user interface where issues can be reviewed and sorted,
   and checked off as resolved.

Two plugins are required

+ [The local plugin](https://moodle.org/plugins/local_qtracker) which
  implements the question database
+ [The block plugin](https://moodle.org/plugins/block_qtracker)
  which provides the student user interface.

# FAQ

## Why is the QTracker block not showing up in my Quiz activity?  

All Quiz activity modules defaults to hide all blocks during an attempt.
This must be changed in order for the QTracker block to show up for students.
Go to the "Edit settings" for the Quiz activity. Then, under "Appearance", set the "Show blocks during quiz attempts" to `Yes`.

# Where to start 

Welcome to the official user documentation for the [QTracker local module](https://moodle.org/plugins/local_qtracker).

* **Teachers**
  1. [Accessing question issue tracker](Accessing-question-issue-tracker)
  2. [Manually creating a new issue](Manually-creating-a-new-issue)
* **Students**
  1. [Creating a question issue](Creating-a-issue)
* **Administrators**
  * [Installation instructions](Installation-instructions#installation-instructions)
* **[Developers](Developer)**
  1. [Developer docs](Developer)
  2. [Languages](Languages)

# Contributors to the CAPQuiz project

**Project lead**: [Hans Georg Schaathun](http://www.hg.schaathun.net) of the Norwegian University of Science and Technology. Contact at: <hasc@ntnu.no>.

**Initial Development**:
[André Storhaug](https://github.com/andstor) of the Norwegian University of Science and Technology. Contact at: <andr3.storhaug@gmail.com>.
