# Question Attempt Data Model

This diagram shows the key database tables used to record questions and their questions. Most of the tables belong to the Moodle core. The (Jazz)Quiz table is the core table of the quiz activity, and every activity module needs such a table to record activity instances. The Session table is used by JazzQuiz because the quiz is only used in a classroom session, with many students present in one session. This is not necessarily needed by other quiz activities.



![DB Table Diagram](http://confluence.uials.no:8090/rest/gliffy/1.0/embeddedDiagrams/25bfcec4-16fd-4943-8b24-acd67a94ddef.png)

An attempt represents a try on a particular question by a particular student. This part of the data model is explained here:
[Moodle docs](https://docs.moodle.org/dev/Overview_of_the_Moodle_question_engine)

