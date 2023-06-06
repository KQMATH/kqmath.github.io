# Using QTracker as a Teacher

## Enabling the QTracker

To enable the QTracker, we need to add the QTracker block to the 
activity (typically the quiz).  This may vary between moodle versions
and themes; this description is based on the default theme in Moodle 4.1.

Viewing the activity as a teacher, you can open the block drawer on the
right hand side.  Here you should find a choice to «Add a new block».
Click this and choose «Question Tracker».  Now the tracker block should
appear below the «Add a block» button.

To make it appear for the students, we also need to change the settings
in two places.

1. Make sure Edit mode is enabled and open the cog menu in the block.
   Choose Configure Question Tracker block $\to$ Where this block appears
   $\to$ Display on page types $\to$ Any quiz module page.
2. In the Quiz Settings find Appearance $\to$ Show more $\to$
   Show blocks during quiz attempts $\to$ Yes.

## Accessing question issue tracker through the quiz interface

When in the quiz the teacher interface will have a block on the right side of the screen called "Module" Question Tracker.
When "View issues..." is clicked the Question Tracker interface will be opened.

## Accessing question issue tracker through the course interface

When in the course interface click the cog in the top-right of the screen, in the menu press more to go into the course administration page
At the bottom of this page there should be a portion named "Question Tracker", where you can open the question tracker for the entire course

Each question will have a row with the columns:
* Question ID
* Name -> Clicking this value will open a block containing all issues tied to the question
* New -> Clicking this value will open a block containing all new issues tied to the question 
* Open -> Clicking this value will open a block containing all open issues tied to the question
* Closed -> Clicking this value will open a block containing all closed issues tied to the question

Once the block is open you get a few more options:
* At the top of the block there is a separate section "question-name #question-id". Clicking this will take you to the question editing page
* A list of all the issues containing:
  * The username of the issue-creator -> Clicking this will take you to the users page
  * The date the issue was created
  * The title of the issue -> Clicking this will open the issue
  * The issue comment

## Manually creating a new issue

To manually create a new issue you must be logged in as a student.

### Log in as student

To log in as a student, click your profile on the top-right of the screen, regardless of page.
In the menu which now appears, click "Switch role to...". This will open a page where you can simply click the role you wish to be logged in as
To revert this, simply click your profile again and click "Return to my normal role"

Now that you are logged in as a student, open the quiz and create a new issue the same way a student would:
[Create new issue as a student](https://github.com/KQMATH/moodle-local_qtracker/wiki/Creating-a-issue)

## FAQ

### Why is the QTracker block not showing up in my Quiz activity?  

All Quiz activity modules defaults to hide all blocks during an attempt.
This must be changed in order for the QTracker block to show up for students.
Go to the "Edit settings" for the Quiz activity. Then, under "Appearance", set the "Show blocks during quiz attempts" to `Yes`.

