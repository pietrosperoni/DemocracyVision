# Fair Open Poll

This directory should contain a particular case. A very simple system, where people can present their ideas. People are not, in this system, allowed or encouraged to build upon each other idea. And then ideas are evaluated in a fair way.

# Pages:

---

## Landing Page
This website permits you to participate in a fair open poll.

Because we value fairness we shall not tell you more than you strictly need to know until you made your evaluation. In this way 

---
## Log In Page

If you have already registered please Log In to proceed

---
## Register Page

If you have never registered please register to proceed

---
## Question Page

The question you have been invited to evaluate is:

...

Do you have an answer to this?

* **Field**: Write an answer

* **Button**: I do not have an answer, let me evaluate other's answers.

* **Button**: I do not have an answer, but I do not wish to evaluate any more answers for this question. Let me look at other questions.

---
## Evaluate an Answer Page

The question you have been invited to evaluate is:

...

Here is a possible answer:

...


* **Stars**: Evaluate this answer

* **Button**: let me evaluate other answers. Greyed until the answer is evaluated

* **Button**: I do not wish to evaluate any more answers for this question. Let me look at other questions.

NOTE: When a proposal is evaluated, the author should receive an email: Hey, your proposal has been evaluated. You have so far received ... evaluations. With this spectrum, and this average.


---
## See the Results Page

**NOTE**: By looking at this page you give up the possibility to evaluate other proposals in future on this question.


The question was:

...

Here are the answers [in order of average vote received]:

1. ... written by: ... (spectrum of the number of votes received) (average vote received) (number of people to which it was presented)
2. ... written by: ... (spectrum of the number of votes received) (average vote received) (number of people to which it was presented)
3. ... written by: ... (spectrum of the number of votes received) (average vote received) (number of people to which it was presented)


...

---
---

# Behind the scenes

The database should keep track of everything and use to make sure proposals are evaluated in a fair way.

When a person asks to evaluate a proposal he is given a random proposal to evaluate *among the ones that has been evaluated less times*.


# The Database

## Tables

* **Users**. Columns: id, username, facebook number, password (coded with a seed), last time the user has participated, self description, gender, homepage.

* **Proposals**. Columns: id, question id, blob, author, time in which it was presented, number of people to which it was presented, number of people that succesfully evaluated it.

* **Questions**. Columns: id, author, blob, time in which it was presented.

* **Votes**. Columns: id, author, proposal, time of presentation of proposal, time of vote.




















