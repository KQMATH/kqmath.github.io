# Attempts report

The CAPQuiz attempts report allows the teacher to see a table of student's attempts for a CAPQuiz, with a row for each attempt. It primarily shows all the related question- and user ratings tied to one particular CAPQuiz attempt (one row). In addition, it also possible to show the answer state, the question text, the student's response or the right answer.

## Report columns
### First name / Surname
The student's first and last name.

### Email address
The student's email address.

### User id (download only)
The id of the Moodle user.

### Moodle question id (download only)
The id for the Moodle question.

### Answer state
One may chose to show the answer state. 

The answer state may be one of the following:
* **gradedright** - The student answered correct
* **gradedwrong** - The student answered wrong
* **todo** - The student started an attempt, but has not yet answered.

If the state is considered "correct", a ✅ green checkmark prepends the text. If it is interpreted as "wrong" , the text is prepended with a ❌ red cross.

### User rating
The student's rating before the student answered the question.

### Previous user rating
The student's rating after the student answered the question.

### Question's previous rating
The question's rating after the student answered the question. If the (previous) question rating was made by the teacher, and not as a result of student attempts, a ⚠️ warning sign is displayed in front of the rating.

### Previous rating was manually updated (download only)
If the question rating was made by the teacher, and not as a result of student attempts, this column will be set to true. Otherwise, false (or null if nonexistent). This is only tied to the previous question rating.

### Time answered (download only)
The date 📆 (D:M:Y) and time 🕐 (H:M:S) the question in the attempt was answered.

### Time reviewed (download only)
The date 📆 (D:M:Y) and time 🕐 (H:M:S) the question answer was reviewed in the attempt.

### Question text
The question's text. This is what the student is suppose to "answer". This is particularly helpful when the question is randomized.

### Response
One can show the student's response. This is what the student chose to answer. A ✅ green checkmark prepends the response text if it was correct. However, if it was wrongly answered, the text is prepended with a ❌ red cross.

### Right answer
One can show the right (correct) answer to the question. This is particularly helpful when the question is randomized.

## Table preferences
### Sorting columns
The table may be sorted by a particular column. This is done by clicking on the header of the preferred column. Clicking again on the same header results in a reverted sorting order.

### Hiding columns
One may hide a column by clicking the minus sign in the preferred column's header.

### Resetting preferences
One may reset all table preferences by clicking the link `Reset table preferences` at the top right of the table. 

## Exporting the report
It is possible to export/download the attempts report. Just select one of the file types in the dropdown menu located at the top of the table and click on the `download` button.

The file types available depends on the installed set of Moodle [Data formats](https://docs.moodle.org/dev/Data_formats). Moodle ships with a set of Data formats natively, including CSV, Excel, ODS, JSON, and HTML. The report may be exported/downloaded in all the installed Moodle Data formats.