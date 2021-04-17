# Things to remember if you run the Moodle Server

This is not meant as an official instruction, but rather a checklist
for installations in our use context, in case it be useful to others.

1. Enable [multiple languages content filter](https://docs.moodle.org/38/en/Multi-language_content_filter)
   This allows multiple languages coded in questions texts, with moodle displaying only the language selected in the student's profile.
2. Remember to configure STACK and select the right version of Maxima (log into the server and run maxima to see the version).

## User (Student) Management

If you run a rogue server, without administrative support to enrol
students, you will probably want the students to self-enrol.
Both site- and course-level configuration are needed.

### Site-level configuration

1.  Self-registration:
    Site administration → Plugins → Authentication → Manage authentication
    - Enable Email-based self-registration
    - Make sure Self registration is not on disabled
2.  Auto-Enrol
    Site administration → Plugins → Enrolments → Manage enrol plugins
    - Enable auto enrolment
    - Open settings and choose when users will be enrolled

### Course-level configuration

Self-enrolment must be enabled for each course as desired.

Enterring the course as a teacher, one can choose

1. Course settings menu (gear icon). If there are two gear icons, then the upper one is for the course and the lower one for the activity. Use the upper one.
2. More ...
3. Users (tab)
4. Enrolment methods
5. Enable self-enrolment (student). This is the eye icon on the appropriate line.

The configuration may be tuned to select the gear icon on the self-enrolment line. As far as I can see, the defaults are fine. If one runs the same module several times, one may consider unenrolling inactive users.

## Creating Teacher and Admin Users

### Admin users

There is always one admin user created at installation time, and this may suffice.

If personal accounts should have admin priviliges, this is set under Site administration → Users → Permissions → Site administrators

### Autonomous teachers

Teachers using the moodle installation should be Course *Creators*,
which means that they can create new courses at whim.

An account can be assigned the course creator role from Site administration → Users → Permissions → Assign system roles

If the teachers are not course creators, an administrator needs to create every course needed.

### Course teachers

The user creating a new course will normally be a teacher on that course.

**TODO.** How to define additional teachers.
