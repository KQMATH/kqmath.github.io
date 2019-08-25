# Editing a Quiz
The teachers interface for CAPQuiz consists of a number of tabs.

## Dashboard
The dashboard provides some status information about the quiz instance. Also, the controls for [publishing a quiz](https://github.com/KQMATH/moodle-mod_capquiz/wiki/Publishing-a-quiz) and making a [question list template](https://github.com/KQMATH/moodle-mod_capquiz/wiki/Question-list-templates) resides here.

## Matchmaking
Two selection strategies have been implemented, but only N-closest is adaptive. Chronological is for testing.

### N-closest
The teacher chooses the desired probably that the student answers correctly (Desired user win probability). Based on this probability and the student rating, the system determines the ideal question rating.

The system takes a set of questions with rating closest to the ideal question rating. The teacher chooses the number of questions to draw. From this set, the student is given a question uniformly at random.

The teacher can also select a blacklist period, to avoid questions from being repeated. ( Prevent the same question to be used for N attempts ).

## Rating system

The rating system is based on the
[Elo rating system](https://en.wikipedia.org/wiki/Elo_rating_system).
The questions and the students have different K-factors which can be 
set independently.

The student K-factor should be seen in relation to the desired win 
probability under *Matchmaking*.  If the student answers incorrectly
he looses rating points calculated as K times the estimated win 
probability.  If he answers correctly he gains rating points given as
K times 1 less the estimated win probability.  
A lower K-factor means that the students answer more questions to 
reach their target.  A higher K-factor may leave the students answering
the same questions many times, even if they are answered correctly, 
especially if there are relatively few questions in the list.

**Example**
I.e. if the desired
win probability is 75%, we expect a student answering perfectly to
gain K/4 points per question on average.  With K=32, it thus takes
about 100 questions to rise from 1200 to 2000 rating points.
(This is a rough estimate which depends on the number and distribution
of questions.)

The question K-factor is less critical for the student experience.
Keeping it low means that the ratings are fairly stable, and the 
students with the same rating get the same number of rating points
for answering the same question.
Higher K-factors may be necessary with a new question list where
the ratings are not expected to be good estimates of the actual
difficulty.  The higher K-factors means that the ratings will 
adapt to relative student performance, but random factors get more
influence on the activity.

## Question
This is where the list of questions is composed. The interface is similar to that of [JazzQuiz](https://github.com/KQMATH/moodle-mod_jazzquiz), with the question list on the left and the question bank on the right.

In the question list, there is a field to change the question's rating. Note that the same question may have different ratings in different question lists. **The rating is only updated when the user presses Enter in the input field.**

## Badges
To change the thresholds where new stars are gained.

## CAPQuiz
To change name and default user rating.

The default user rating is the initial rating assigned to new students joining the activity.

## Class list
For [reviewing a quiz](https://github.com/KQMATH/moodle-mod_capquiz/wiki/Reviewing-a-quiz).
