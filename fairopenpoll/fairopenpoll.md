# Fair Open Poll

This directory should contain a particular case. A very simple system, where people can present their ideas. People are not, in this basic system, allowed or encouraged to build upon each other idea. And then ideas are evaluated in a fair way.


# Pages:

---

## Landing Page
This website permits you to participate in a fair open poll.
Because we value fairness we shall not tell you more than you strictly need to know until you made your evaluation. 

---
## Log In Page

If you have already registered please Log In to proceed

---
## Register Page

If you have never registered please register to proceed.

The page will gather the email and password.

---
## User Page

Some questions asked are only open to some users, others will make the results representative of some population, thus making sure each proposal is evaluated by people in the correct proportions for some characteristics. For this reason we are now asking you some personal details. You do not have to answer any. But the more you answer, the more questions you will be invited to participate. And please answer truthfully or the results will be less reliable.

Name: (Your name will appear on the proposal you have suggested, after the evaluation is over)
Sex:
Year of Birth:
City of Residence:

(more details will appear once we are required by the people asking the questions to use them)


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


* **10 Stars**: Evaluate this answer. 

* **Button**: let me evaluate other answers. Greyed until the answer is evaluated

* **Button**: I do not wish to evaluate any more answers for this question. Let me look at other questions.

The on the side:

* **Button**: FLAG: [NOT ANONYMOUS] The proposal is not anonymous
* **Button**: FLAG: [OUT OF SCOPE] The proposal is out of scope respect to the question
* **Button**: FLAG: [NOT AN ANSWER] The proposal does not answer the question
* **Button**: FLAG: [ILLEGAL] The proposal is illegal
* **Button**: FLAG: [UNCOSTITUTIONAL] The proposal is against the constitution
* **Button**: FLAG: [AGAINST INTERNATIONAL TREATIES/HUMAN RIGHTS] The proposal is against international treaties, Human Rights, ...

NOTE: Flags are available at any time. When a proposal is flagged, it gets temporarily extracted from the page, and sent to either an administrator (for the first three), or to an administrator who is also a lawyer. If the admin finds the proposal ok, it is brought back, and from that moment that particular flag cannot be raised again for that proposal (it will appear greyed).

NOTE: When a proposal is evaluated, the author should receive an email: Hey, your proposal has been evaluated. You have so far received ... evaluations. With this spectrum, and this average.





---
## See the Results Page

**NOTE**: By looking at this page you give up the possibility to evaluate other proposals in future on this question.


The question was:

...

Here are the answers [in order of average vote received]:

1. ... written by: ... (spectrum of the number of votes received) (average vote received)(error on the measurement)
2. ... written by: ... (spectrum of the number of votes received) (average vote received)(error on the measurement)
3. ... written by: ... (spectrum of the number of votes received) (average vote received)(error on the measurement)


...

---
---

# Behind the scenes

The database should keep track of many other details to make sure proposals are evaluated in a fair way.

When a person asks to evaluate a proposal he is given a random proposal to evaluate *among the ones that has been evaluated less times*.

The administrators who define a question should also define who is the question open to, and what personal characteristics should be considered when finding users to evaluate proposals, as well as what percentage should it approximate.

For example an administrator should be define a question as open to anyone living in Bologna, and the question balanced to reflect a population of 51% female and 49% male (because this is the gender balance in Bologna -I am making those data up-).


# The Database

## Tables

* **Users**. Columns: id, email, password (coded with a seed), last time the user has participated, facebook number, twitter number, rome[user/administrator/administratorlawyer].

* **UsersData**. Columns: id, Users:id, Real Name, gender, Year of Birth.
[More columns will appear here as policy makers ask questions to people from only some places, or only of a certain education level, and so on]

* **Proposals**. Columns: id, question id, title [max 140 ch], summary [max 1500 ch -usually used only max 900-], blob, authordescription, author:id, time in which it was presented, number of people to which it was presented, number of people that succesfully evaluated it, flag:anonymous [yes, no, maybe, tochech],flag:outofscope [yes, no, maybe, tochech], flag:notanswering [yes, no, maybe, tochech], flag:illegal [yes, no, maybe, tochech], flag:uncostitutional [yes, no, maybe, tochech], flag:againstIntLaws [yes, no, maybe, tochech].
[all the flags are set to maybe. When someone raises a flag that goes to check. Then the admin decides if they are to on or to off.]

* **Questions**. Columns: id, author, blob, time in which it was presented.

* **QuestionsRequirementToParticipate**. Question:id, UsersData:nameofcolumn, valueaccepted.
* **QuestionsBalance**. Question:id, UsersData:nameofcolumn, valueaccepted. 
[those two tables are still the less clear]

* **Votes**. Columns: id, author, proposal, time of presentation of proposal, time of vote.





















