---
title: "Disease, Epidemics and Vaccination Effectiveness through Agent Based Modelling"
excerpt: "This project involved using computational modelling to look at how vaccines affect disease spread. <br/><img src='/images/standard_disease_spread.gif'>"
collection: portfolio
---

Overview
======
This project involved using computational modelling to look at how vaccines affect disease spread. The goal of the
project was to see the effectiveness of vaccines to slow and stop the spread of disease. The model consisted of people
who randomly moved around in the environment, and these people could be healthy, sick, or dead as well as have been 
vaccinated or not. As people moved around the disease could spread based on various parameters such as
the distance between people, the infection rate of the disease, and the vaccine effectiveness. The simulations for
the model can be visualized as seen below.

<img src='/images/standard_disease_spread.gif' class='center'>


The Problem
======
During my undergraduate degree, I took a course called ENGG*3130-Modelling Complex Systems. This course focused on
looking at complex global and socioeconomic issues using computational modelling in Python. As part of the course,
I was involved in a team of three to model a complex issue using the techniques discussed in the course.

The issue my team and I tackled was to model how disease spreads and vaccine effectiveness through the use of 
agent based modelling. Agent based modelling involves modelling a system using a collection of autonomous 
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


<img src='/images/model_at_diff_stages.svg' class='center'>


The Result
======

Further Information
======
The project can be found in my GitHub profile or by using this link: 
[disease-agent-model](https://github.com/szentimh/disease-agent-model).

