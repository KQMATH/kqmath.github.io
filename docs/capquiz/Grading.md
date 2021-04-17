
CAPQuiz supports grading. Internally the students are assigned a rating, using the [Elo rating system](https://en.wikipedia.org/wiki/Elo_rating_system) which is known from chess. Note that the Elo system is equivalent to the [Rasch model](https://en.wikipedia.org/wiki/Rasch_model) but uses different scaling factors.

# Grading

The rating is translated into a number of stars, using configurable thresholds. The number of stars achieved can be transferred to the grade book for the course, as a grade. In the grading tab, you may set the required number of stars⭐️ for a passing grade. The default is ⭐️⭐️⭐️ 3 stars. A deadline must be set. If no deadline is desired, it can be set some decades into the future, which should suffice in practice.

A temporary grade, i.e. current number of stars, is transferred and updated continuously in the grade book. Once the deadline passes, this grade is permanent, and no longer updated.

Students can continue working on the activity after the deadline, it just does not affect the grade. The student is informed about this in the attempt page.

In the class list, within CAPQuiz, the instructor can see both the grade (number of stars at the deadline) and the current number of stars. Before the deadline these two numbers are equal.  After the deadline they may differ.

# Rating

Both students and questions are assigned a rating, representing aptitude and difficulty respectively.  The starting rating is typically 1200. Each time the student answers a question, their rating is updated.  If they answer correctly, their rating increases by K*(1-1/(1+10^(Rq-Rs)/400, where Rq and Rs are the question and student ratings respectively, and K is the student k-factor which can be set in the *rating system* tab. If the student answers incorrectly, their rating decreases by K/(1+10^(Rq-Rs)/400.

Question ratings are updated in a similar way, but not based on their performance against a question.  Instead two consecutive questions answered by the same student are compared.  If one is answered correctly and the other incorrectly, this constitues a match where the incorrectly answered question `wins´.  Rating updates for questions are based on these matches.

# Question selection strategy

The question selection strategy is also configured in the *rating system* tab.  Chronological is non-adaptive, so we assume that N-closest is used.  The teacher selects the desired user win probability, i.e. the probability that the student answers correctly according to the Elo model. This translates into a target question rating. If the win probability is set to 0.5, the target question rating is equal to the student rating.  Higher probability gives easier questions and vice versa.

The system takes the N questions closest to the target rating.  This `number of questions to draw' is configurable as well.  From among these N questions, one is drawn uniformly at random.  It is possibly to blacklist questions so that they do not reoccur for a number of attempts.  This number is set in the field for `Prevent the same question to be used for N attempts'.