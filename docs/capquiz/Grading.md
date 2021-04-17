# Grading

CAPQuiz supports grading. Internally the students are assigned a rating, using the [Elo rating system](https://en.wikipedia.org/wiki/Elo_rating_system) which is known from chess. 

## Grading

The rating is translated into a number of stars, using configurable thresholds. The number of stars achieved can be transferred to the grade book for the course, as a grade. In the grading tab, you may set the required number of stars⭐️ for a passing grade. The default is ⭐️⭐️⭐️ 3 stars. A deadline must be set. If no deadline is desired, it can be set some decades into the future, which should suffice in practice.

A temporary grade, i.e. current number of stars, is transferred and updated continuously in the grade book. Once the deadline passes, this grade is permanent, and no longer updated.

Students can continue working on the activity after the deadline, it just does not affect the grade. The student is informed about this in the attempt page.

In the class list, within CAPQuiz, the instructor can see both the grade (number of stars at the deadline) and the current number of stars. Before the deadline these two numbers are equal.  After the deadline they may differ.

# Rating

Both students and questions are assigned a rating, representing aptitude and difficulty respectively.  The starting rating is typically 1200. Each time the student answers a question, their rating is updated.  If they answer correctly, their rating increases by \[K*(1-1/(1+10^(Rq-Rs)/400\]