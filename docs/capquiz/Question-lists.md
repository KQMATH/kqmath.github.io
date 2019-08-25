# Question lists

The critical element of CAPQuiz is the question list.
The question list is a collection of questions from the Moodle
question bank with difficulty ratings.  
Setting up a CAPQuiz activitity, the curation of the question list
is always the most important and time-consuming task.

In the current implementation, there is a one-to-one correspondence
between activity instances and question lists.  I.e. each activity
uses one question list and each question list can only be used by
one activity.  This means that when the question difficulties are
reestimated because of student results in one activity, it has no
bearing for other student cohorts using a different activity instance.

Sharing question lists between activities or courses is possible via 
[question list templates](https://github.com/KQMATH/moodle-mod_capquiz/wiki/Question-list-templates).
A question list template is a read-only copy of a question list,
effectively created as a snapshot of the question list from some
activity instance.
When a new activity instance is created, the question list can be
created by copying an existing template, instead of starting from 
scratch.  This is the only way to reuse material within CAPQuiz.

