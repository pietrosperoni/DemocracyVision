Democracy Vision
==================


Authors:
------------

Pietro Speroni di Fenizio  
... *(add your name here)*  


# Introduction #

The idea behind this democracy system is to create a system where everybody can participate in the actual legislative process. Not just in voting representatives, or voting the possible laws. A problem with this is that laws are often too complex for people to participate. As a result only technicians are usually discussing something. But in many representative democracies there are technicians that collaborate with policymakers to

1. explain them the subtleties of a topic
2. explain them what a law actually mean
3. translate into law the general idea that the policymakers usually had.

This because policymakers in modern representative democracies are often not technicians. And are usually elected because of their popularity and their (presumed) ethical positions. And not because of their technical skill.
So in our system proposals are expected to include a both a technical part and an explicative part, so they can be understood by the general public. More than this proposals will be evaluated not just respect on how people agree with them, but how much they are understandable. As such people with technical skill will have an extra opportunity to participate by being able to re-write proposals to make them more understandable. 


# Principles: #


## Fairness ##

Proposals should be evaluated just on the base of their content.

# Function: #


Every person can suggest a proposal. People who like the proposal can support them;

*(note: issues with fairness. Should proposals be polled?).*

People who partially like the proposal should fork it, and change it in a way they like. And then support that. It is assumed that anyone supports its own proposals. Once a person supports a proposal he should be told (receive via emails) all the forks that happen to it. In this way he can follow the river of the discussion, and keep supporting the ideas that are acceptable to him.  

**This requires to develop**:  

A way to view the graph of the proposals. Seeing which parts you like, don't like, and don't understand. This could be done with colors. Green, means I like (yey!). Red means I don't like (ugh!). Grey, means I don't understand (uh?). White means I don't care (bah!). And you just go continuously from one to the other.  

First problem: supporting a proposal is not the same as following a project on github. In github you "follow" a branch. So one after the other. In demhub you must approve each version, but. But if you approve a version, and another version, we can assume you approve all the middle versions.

#Evaluation.#

##How are proposal evaluated:
  
Each proposal should be evaluated on a two-dimensional continuous inverted triangle format. Having the vertical line representing personal understanding of the proposal. And the horizontal line representing how much the person agrees with it. Having on the top left “I understand it but I don't agree with it”. On the top right “I understand and agree with the proposal”, and on the bottom “I don't understand the proposal”. The central line will then represent people who understand (at various level) the proposal, but are essentially neutral about it. When people will evaluate a proposal the triangle with pop up, and the person will be allowed to click where they agree.

    ___________________
    \        |        /
     \       |       /
      \      |      /
       \     |     /
        \    |    /
         \   |   /
          \  |  /
           \ | /
            \|/
             '
**Notes**:  
Being continuous people will tend to vote with the belly. #at least this is what I have been told it happens
Also this does not really consider the difference between people that agree that something is done, or that are willing to act personally so that it gets done. Similarly it does not distinguish between people that are essentially against a proposal, and people that veto it, and would actually fight to make sure that it does not pass. All this would make a really interesting expansion.
Another big problem with this has to do with people claiming that they understand a proposal more than they really do. One way that we can make sure this is limited is by asking people to participate in a measure that is proportional to how much they claim they understand the proposal. For example answering questions about the proposal. Or forking and rewriting the proposal. And if they cannot we expect (track?) their understanding going down. But of course a problem with this is that people might claim they did not understand the question, or they have no time to answer those questions.

## How the evaluation information is used: ##

**Asking people to rewrite proposals**:

Demhub will use this information to find out:

1. who understands and likes a proposal.
2. how many people do not understand a proposal
3. This will help to understand what proposals are clear and which one are not. 

Demhub will then automatically find people who are

1. good in writing proposals
2. understand the proposal
3. possibly even agree with it

And ask them to fork it and rewrite it.

The process would be worth if the new proposal has a higher understanding and agreement than the previous one. In fact once multiple versions of the same proposal are written they should be placed side by side. And the evaluation for the understanding should be done all at the same time.
Similarly comments written, can help to make a proposal more understandable.

**Asking people to merge different proposals.**

Similarly the system can use the information to try to suggest when two proposals could be merged. Sometimes a person that is invited to join two proposals might say that they are actually alternative description of the same proposals. If this is the case the proposals might be considered equivalent (after asking other people). 

## Equivalent Proposals. ##

A possible problem is to identify equivalent proposals. One way is simply to ask people who understand two closely related proposals (one being the daughter of the other) if they are the same. When people fork a proposal they should say if their new version is semantically the same as the previous proposal. In other words if it is simply a new wording of the previous proposal. If this is the case people will be presented both proposals to evaluate at the same time. Side by side. 
This information should be used to guide the people in the way they agree with the proposal. In other word if they agree with one they cannot disagree with the other. But they could not understand the other. Suppose we have two proposals A and B. And a person p votes that he likes A 3/5 and understands it 4/5. Then his  position would raughly be where the dot is:

    ___________
    \    |    /
     \   |  ./
      \  |  /
       \ | /
        \|/
         '
Now let us suppose that he understand the (equivalent) proposals B 3/5. Then he can only like it, with the two dots representing possible alternative votes:

    ___________
    \    |    /
     \   |   /
      \  | ..
       \ | /
        \|/
         '
But in fact the situation is more complex than that because two proposals equivalent can induce a person to understand either of them more than if the person has read only one of them. So the best would be that once you have multiple equivalent proposals a person votes for them all at the same time. The proposals would essentially be merged for what concerns the voting procedure. (Of course not for what concerns the forking procedure, where the grammatical way a proposal is presented comes back to be really important). Of course a person can just claim that the two proposals are not really equivalent. In which case I am not sure what happens. He probably must claim to understand them both at a high enough level.

## Following versus supporting ##

So now we have a family of proposals. Divided in branches. Is it correct to have them divided in branches? Isn't this giving power to the maintainer of a branch? In a sense following a branch is a form of liquid democracy: you trust the maintainer of the branch. An alternative would be that every time there is a new version people are invited to evaluate it. A problem with this is that too much proposals would need to be evaluated. It could be enough if people can follow the daughters of a proposal, but not a branch. And only be invited to vote when someone declares a proposal as being a milestone (@mbarkhau suggests this being equivalent to a request for pull. Something that simply does not exist in a fully distributed system).

If proposals are connected via git style connection, they are really all part of a graph. As such they don't need to be clustered that much. Still it might be possible to visualize the graphs in 3D with the height represented by how understandable (on average) a proposal is. People will start to read proposal that are more understadable, and them move from there down, as they enter into the topic. Also they should read proposal that are understandable and representative of many people. Maybe each proposal could be seen as an island. With the size being how many people approve it, and the height how much it is understood. In fact maybe each person vote could be represented as a dot, of a certain height, around the proposal. Of course the result of this is that each proposal end up having a peak of the same height, the highest. As all the proposals will have a person (the author) who claims to understands it fully. 
 
## What needs to be done: ##
how to avoid people just sending a link to a proposal they wrote to all their friends.

