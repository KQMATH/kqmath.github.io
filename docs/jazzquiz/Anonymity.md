This is an on-going discussion on how anonymity can be established.

# Anonomous user in the database

It is not possible to create a question_attempt without a user ID.  As
a minimum, a dummy ID is required to satisfy the API.

There are three alternatives here:
1.  Null user.  This may or may not be possible. 
   Would it be equivalent to allowing guest users?  See below.
2.  User ID is deleted from question_attemots after each question.
2.  User ID is deleted from question_attemots after each session.

# Anonomous user in the frontend

One alternative is to the user be anonymous only in the frontend.
Then, the ID is stored for each answer in the database, but there
is no way to see the ID in the user interface.
This is what ActiveQuiz does.

Alternatively, student IDs for each answer can be made available to 
admin but not to the teacher.

# Class list

Even when answers are anonymous, it is an advantage to be able to
get a class list showing participation.

# Guest user

Is it possible to let a guest user take quiz?

We have not yet figured out how.  There is no apparent way to validate
an answer without a UI.

# Summary

In order of priority
1.  Make all reports, except the classlist, anonymous. 
2.  Allow anonymous sessions, where the link to the user ID is severed
  at some point in the process.
3.  Support classlists, even for anonymous sessions. (Can be made optional.)
4.  Allow non-anonymous sessions.

Anonymous sessions should be the default.

