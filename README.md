# Thesis Discussion

Design a path-tracking controller for a platoon of vehicles that is shown to have a guarantee for lateral bounds during lane change maneuvers.

## Why?

(In brief) Platooning of vehicles has been shown to have [increased fuel efficiency, improved highway efficiency and reduced emissions](https://www.hindawi.com/journals/jat/2020/2604012/). Especially in the application of freight trucks, platooning of vehicles can be greatly used to reduce the costs of transportation. Given the fact that most of the journey of the platooning vehicles would be in a structured environment (highways) with less number of disturbances, the possibility of actual implementations of vehicle platooning is quite and hence it's an exciting field of research to look into

## Problem Definition

Essentially, we're trying to design a trajectory tracking controller for every vehicle in the platoon. With the possibility of vehicle communications between the vehicles, taking that to our advantage, we're looking to design a controller that would give us a real tight spacing between each vehicle in the platoon while maintaining enough spacing to avoid head-on collisions. Safety is the main aspect we're taking into consideration here, therefore our path tracking controller must be able to give us a safe trajectory to follow at all times.  

*TODO: Add more details here*

## Safety

Since safety is the main aspect that we are taking into consideration, it is useful to define our safety metrics at this point. What are the metrics of safety?

- Avoid head-on collisions with the vehicle in front, in the string, that is, have longitudinal position bounds for every vehicle in the string
- Have lateral bounds for every vehicle in the string - This is especially important for lane change maneuvers
- Since vehicle communication is involved, have emergency vehicle maneuvers in place (*TODO*)
- Take into consideration <u>delays of vehicle communication</u> and design a proper path-tracking strategy
- In case of quick turning at high speeds, there is a possibility of <u>rollover</u> and <u>sideslip</u> occurring that needs to be taken into consideration 

Technical Definitions:

- Stability

#### 1) Definition 1 (String Stability)

String Stability refers to the dampening of errors have we move along in the string. Since We're looking to define a combined controller, we would want string stability in more than one direction



## Description of Strings

The string is designed in the following manner:

There is one vehicle initially, that is the leader of the vehicle. It is assumed to be a vehicle who's trajectory the other vehicles are looking to track. 

> If the lead vehicle is an autonomous vehicle, designing a decentralized controller taking path planning into consideration is an interesting problem to look at! What are the merits and demerits of a decentralized controller?

Design Parameters:

- Lane Width -- Needed for defining the lateral bounds of the vehicle
- Vehicle Dimensions -- For a tighter bound and taking into critical rollover conditions? **Not required**





## Literature Review Papers and their contributions

