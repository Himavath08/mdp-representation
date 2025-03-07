# MDP REPRESENTATION

## AIM:
The aim of this experiment is to create a Markov Decision Process (MDP) representation and implement it in Python to model the decision-making process in a traffic signal system.
## PROBLEM STATEMENT:
### Problem Description
Traffic signal is to control optimization,there is traffic congestion in urban areas is a signifficiant issue leading to increase travel time  fuel comsuption and pollution.

### State Space
* Number of vehicle waiting at each lane.
* waiting time of oldest vehicle at each lane.
### Sample State
* North lane 10 vehicles in 30 seconds
* South lane 15 vechicle in 20 seconds
* East lane 10 vechicle in 45 seconds
### Action Space
* Switch from North-South ,North-East to green
* Switch east to North, east-south to green
* Switch South to North, South-east to green
* Extenend the time interval by green phase 

### Sample Action
The action changes the traffic signal phase to allow East traffic to move along the north south traffic 

### Reward Function
* +1 for moving the vehicle at green light
* -1 for making the traffic  

### Graphical Representation
![WhatsApp Image 2025-03-07 at 13 53 48_dd772062](https://github.com/user-attachments/assets/4a461465-421d-4f35-a47e-2665e445ff5c)

## PYTHON REPRESENTATION:
```
 = {
    0: { 
        1: [(0.4, 2, 0.0, False), (0.4, 3, 0.0, False)], 
        0: [(0.4, 3, 0.0, False), (0.4, 1, 0.0, False)],
        0: [(0.2, 0, 0.0, True), (0.2, 0, 0.0, False)]   
    },
    1: {  
        1: [(0.4, 2, 0.0, False), (0.4, 0, 0.0, False)],  
        0: [(0.4, 0, 0.0, False), (0.4, 2, 0.0, False)],
        0: [(0.2, 0, 0.0,True),(0.4, 1, 0.0,False)]  
    },
    2: {  
        2: [(0.6, 1, 0.0, False), (0.4, 2, 0.0, False)], 
        1: [(0.6, 2, 1, True), (0.4, 2, 0.0, False)], 
        0: [(0.2, 3, 0.0, True), (0.2, 2, 0.0, False)]  
  
    }
}

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/d7d62467-c6c9-45ec-a126-bf0445dc67c3)


## RESULT:
The Markov Decision Process (MDP) has been successfully represented using Python dictionaries. Each state-action pair contains information about possible transitions, transition probabilities, associated rewards, and whether the next state is terminal or not. This representation can be used for further analysis and decision-making algorithms such as reinforcement learning.
