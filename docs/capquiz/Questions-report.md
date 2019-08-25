# Questions report

The CAPQuiz questions report allows the teacher to see a table of question ratings for questions used in a CAPQuiz. One row for each question rating. It provides a historical log of question rating updates tied to user attempts. Hence, it may be used to track each question's rating development. Primarily it shows the question's "new" rating and the question's previous rating. In addition, it also possible to show the question text.

## Report columns
### Attempt id (download only)
The id of the CAPQuiz attempt in which the rating update was done in.

### Question id
The id for the CAPQuiz question.

### Question rating
The question's rating before the student answered the question.

### Previous question rating
The question's rating after the student answered the question. If the (previous) question rating was made by the teacher, and not as a result of student attempts, a ⚠️ warning sign is displayed in front of the rating.

### Rating was manually updated (download only)
If the question rating was made by the teacher, and not as a result of student attempts, this column will be set to true. Otherwise, false (or null if nonexistent). This is only tied to the previous question rating.

### Moodle question id
The id for the Moodle question.

### Question text
The question's text. This is what the student is suppose to "answer". This is particularly helpful when the question is randomized.

### Time created
The date 📅 (D:M:Y) and time 🕐 (H:M:S) the question rating update was done at.

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