MDP REPRESENTATION
AIM:

MARKOV DECISION PROCESS (MDP) REPRESENTATION
 **PROBLEM STATEMENT**  

DEVELOPING A POLICY TO MANAGE A CAR ENGINE'S HEAT LEVEL EFFICIENTLY WHILE OPTIMIZING THE EXPECTED CUMULATIVE REWARD**  

 **PROBLEM DESCRIPTION**  

THE GOAL OF THIS PROBLEM IS TO DEVELOP A POLICY THAT EFFICIENTLY MANAGES THE ENGINE'S HEAT LEVEL IN A CAR WHILE OPTIMIZING THE EXPECTED CUMULATIVE REWARD.  
 **STATE SPACE**  

THE STATE SPACE CONSISTS OF TWO POSSIBLE STATES:  
- **"COOL"** (REPRESENTING A COOL ENGINE TEMPERATURE)  
- **"HOT"** (REPRESENTING A HOT ENGINE TEMPERATURE)  

 **SAMPLE STATE**  

A SAMPLE STATE MIGHT BE **"COOL,"** INDICATING THAT THE ENGINE'S TEMPERATURE IS CURRENTLY AT A SAFE AND ACCEPTABLE LEVEL.  **ACTION SPACE**  

THE ACTION SPACE INCLUDES TWO AVAILABLE ACTIONS:  
- **"ACCELERATE"** (TO INCREASE THE ENGINE'S HEAT LEVEL)  
- **"BRAKE"** (TO DECREASE THE ENGINE'S HEAT LEVEL)  

 **SAMPLE ACTION**  

A SAMPLE ACTION COULD BE **"BRAKE,"** INDICATING THAT THE DRIVER HAS CHOSEN TO APPLY THE BRAKES IN ORDER TO REDUCE THE ENGINE'S HEAT LEVEL.  

**REWARD FUNCTION**  

THE REWARDS ARE STRUCTURED TO ENCOURAGE ACTIONS THAT MAINTAIN THE ENGINE IN THE **"COOL"** STATE (**REWARD OF 1.0**) AND PENALIZE ACTIONS THAT LEAD TO THE **"HOT"** STATE (**STRONG PENALTY OF -10.0**).

Graphical Representation
![265317628-c6ec3554-ea31-4e5a-b72c-fcf50fcb470e](https://github.com/user-attachments/assets/9a0a97d6-e923-4ff2-9885-de887fa4211e)


 PYTHON REPRESENTATION:
```
mdp = {
    "Cool": {
        "Accelerate": [
            (0.2, "Cool", -10.0, False),
            (0.8, "Hot", -10.0, False),
        ],
        "Brake": [
            (0.9, "Cool", 1.0, False),
            (0.1, "Hot", -10.0, False),
        ],
    },
    "Hot": {
        "Accelerate": [
            (0.6, "Cool", 1.0, False),
            (0.4, "Hot", -10.0, False),
        ],
        "Brake": [
            (0.3, "Cool", 1.0, False),
            (0.7, "Hot", -10.0, False),
        ],
    },
}
```

 OUTPUT:

![image](https://github.com/user-attachments/assets/fb4401f1-26d5-4ca6-8d0d-32b9be70d053)



 RESULT:

Thus, a Markov Decision Process (MDP) problem is represented in the following ways:

Text representation
Graphical representation
Python - Dictonary representation


