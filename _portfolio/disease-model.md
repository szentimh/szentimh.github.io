---
title: "Disease, Epidemics and Vaccination Effectiveness through Agent Based Modelling"
excerpt: "The portfolio is currently a work-in-progress.<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Overview
======



The Problem
======
During my undergraduate degree, I took a course called ENGG*3130-Modelling Complex Systems. This course focused on
looking at complex global and socioeconomic issues using computational modelling in Python. As part of the course,
I was involved in a team of three to model a complex issue using the techniques discussed in the course.

The issue my team and I tackled was to model how disease spreads and vaccine effectness through the use of 
agent-based modelling. Agent-based modelling involves modelling a system using a collection of autonomous 
entities interacting with other agents and the surronding environment. 
The goal of the model was to mimic the
movements of people as well as disease spread, and to see the effect vaccination would have on the population. 

The Data 
======
For this project no external or internal dataset was used.

The Model
======
There are two main components to the model; the environment and the agents.

The environment consists of a grid, where each cell can be empty or occupied by an agent. The environment also
stores information about the disease's behaviour, such as the distance the disease can spread from one 
person to another. The environment also keeps track of all of the people in the model and how many have passed away.

The agents in the model represent the people in society. People are able to move around to a spot that
is not occupied and is within viewing distance, and they can be vaccinated or not vaccinated as well as be sick,
healthy, or dead. A person with the disease can spread it to other nearby people based on how far it can spread,
the infection rate of the disease, and if that person is vaccinated or not.

The Result
======

Further Information
======
The project can be found in my GitHub profile or by using this link: 
[disease-agent-model](https://github.com/szentimh/disease-agent-model).

