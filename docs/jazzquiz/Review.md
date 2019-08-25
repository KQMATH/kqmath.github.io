# Review and evaluation

## Comparison to other systems

JazzQuiz offers similar functionality to Socrative.

1. A Quiz can be preplanned or improvised.
1. The same basic question types 
        - True/False
        - Short answer
        - Multiple choice (Socrative is limited to five alternatives)
1. Repeat question as vote over given answers

JazzQuiz does everything that Socrative does to satisfaction.
There are a couple of improvements

1. Equivalent answers are counted together, making it easier to read the list of answers.
1. Dim answers instead of deleting them. Dimming is reversible.
1. Merge answers, accumulating the count.
1. Moodle allows multiple logins so that the teacher can hide answers on the projector and show them on his own box.
1. JazzQuiz has optional anonymity.

JazzQuiz offers additional question types, including mathematical questions.

### Login and Anonymity

Students in Socrative are anonymous, making the login process very quick. 
In Moodle and JazzQuiz this can be done in different ways.

If the Moodle server is set up such that the students need to create
accounts, the startup cost is heavy.  However, there are two ways of
making this as smooth as for Socrative.

1.  JazzQuiz sessions may be opened for guest login.
1.  Students can log in to named accounts using FEIDE 
  (i.e. accounts with Norwegian schools and universities)
  or OAuth2 (e.g. Google). 
  This has to be configured on each Moodle server, though.

The JazzQuiz session can be either
1. Fully anonymous where student identities are removed immediately after
   the session and the teacher has no means of viewing them.
1. Anonymous with attendance list, i.e. the teacher gets a list of named
   students attending, but cannot see who answered what.
1. Non-anoymous, giving the teacher detailed reports of the responses of
   every student.

## Mathematical Questions

JazzQuiz has been developed in the context of mathematics education,
and support of mathematical questions types have been very important.
Several alternative exists.

Currently we use and recommend the following options:

1. Multiple choice with MathJax.  Using MathJax, Moodle can render
   mathematical (TeX) notation in any question type, including
   multiple choice.  The teacher needs to be able to write TeX,
   but not necessarily the student.
1. [ShortMath](https://moodle.org/plugins/qtype_shortmath)
   has been developed specifically for JazzQuiz.
   The student gets a maths editor to answer using a mathematical 
   formula.
1. Short answers.  
   Letting the students represent algebraic expressions as ASCII strings
   was surprisingly effective.  Even though the display is not perfect,
   the students had little difficulty in practice.
   This solution may be inferior to ShortMath, but should not be
   discounted.
   It is particularly useful in brainstorming exercises, where some
   students may offer algebraic expressions and others just verbal
   ideas.

Additionally we have considered and tested the following options.

1. [STACK](https://moodle.org/plugins/qtype_stack)
   lets the student answer with algebraic equations which can be
   graded using a CAS engine.
   We have tested this, but in our courses the students do not learn
   to type correct CAS syntax.  In courses where the students need to
   learn this, STACK may be a good choice, but we have not developed
   the idea further.
   In theory, the CAS engine could be used to filter equivalent answers
   for review in JazzQuiz, but this requires further work.
1. Numerical question types, where the student answers with a number.
   The auto-grader can be programmed to allow different levels of precission,
   and this could possibly be extended to group similar questions in the
   JazzQuiz review, but this would require further work.


## Filtering

Filtering refers to the grouping of responses which should be
considered equivalent.
JazzQuiz will always group equal answers together in a bar chart.
It is annoying when semantically equivalent answers are split, because
of syntactic differences, such as whitespace or different case.

So far we have only allowed for manual filtering in the review
interface.  Automatic filtering is difficult and must be done for
each question type.

### Filtering of short answers

Basic filtering of short answers is possible.

- Strip whitespace at beginning and end of the string (I think this is done currently)
- Case insensitive match 

### Filtering of algebraic answers

1. Simple filtering on TeX code (possibly using RegExp) similar to what can be done with short answers
1. CAS filtering.

Advanced filtering is demanding on the teacher, who will need to decide what to filter. Overfiltering risks hiding important insight from the students. Based on experience, there seems that little can be gained by filtering using CAS. Most filtering has to be done manually anyway, and the effort needed to configure CAS filtering for each individual question simply would not be worth it.

CAS is a complicating feature. We see run-away CAS processes on the server. Maxima does not work on docker, and is not always straight-forward to install. Time-outs and other error control strategies may need to be configured. Hence, avoiding CAS greatly simplifies the system.

If we avoid CAS, we can use MathQuill without having to translate from TeX to CAS code. Thus we can get the advantages of WYSIWYG. This might even improve filtering, since the students may write more uniform and well-formated maths, with less variation. This also means that all answer type scenarioes above can be handled in one question type.

