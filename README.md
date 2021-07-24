### Capstone: Predicting NFL play calls.


## Overview

In this README.Md you will find:
- Problem Statement
- Dataset I used
- Preprocessing Techniques
- Brief Summary of Analysis/conclusions

## Problem Statement

Data analytics are becoming an increasingly large part of our lives. Regardless of the industry, it's pretty likely that data analytics can be used to increase one's knowledge or ability in their respective job. This is especially the case in the world or sports. Because of the increase of analytics in baseball, hitters are struggling now more than ever because the pitchers know the exact weaknesses of every player. In the NBA, teams are shooting more 3 point shots because of the analytics. In the NFL, teams are increasingly 'going for it' on 4th down and 2-pt conversions. 

In the National Football League, having a good coach is invaluable. More so than in other sports, NFL coaches have a tremendous impact on the game while it is being played. When calling a play, the playcaller for each team determines the starting position of the players and their responsibility for each play. On offense, the play is usually designed to gain the most yards possible. On defense, the play is usually designed to stop the offense from advancing. Coaches choose plays based off many factors, including what they anticipate the other team to do, situation of the play, score of the game, personnel, formation, previous outcomes of that playcall, randomness, injuries, and sometimes just a gut feeling. If you know what play the other team is going to run, your chances of success are a lot higher. Successful coaches are known to have 'unpredictable offenses', where there's an equally likely chance that a pass or a run is called. I want to investigate which coaches are the most predictable. 

The goal of this project is to build several classification models that predict whether an NFL team is going to pass or throw. I am going to develop multiple models including logisitic regression, KNearestNeighbors, and a Random Forest Classifier. Success will be based on accuracy, how often my model correctly predicts the play that's run. This project will be useful to anyone in the football industry that wants an edge over their opponent.

---
## Datasets

Gathered 2020 play-calling data from http://nflsavant.com/about.php.   

---
## Pre-Processing
Selected only pass and run plays. Selected plays that had no penalties, challenges, or extra points. Dropped columns that had to do with the result of the play, not the play call itself. 

---
## Brief Summary of Analysis/Conclusions

Base-line rate is 58.96% that the play is a pass. No modeling yet, but have looked at trends among different teams. 

---