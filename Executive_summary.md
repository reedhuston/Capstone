### Capstone: Predicting NFL play calls.


## Overview

In this Executive Summary you will find:
- Problem Statement
- Datasets I used
- Data Dictionary
- Preprocessing Techniques
- Modeling
- Metrics
- Brief Summary of Analysis/conclusions

## Problem Statement

Data analytics are becoming an increasingly large part of our lives. Regardless of the industry, it's pretty likely that data analytics can be used to increase one's knowledge or ability in their respective job. This is especially the case in the world or sports. Because of the increase of analytics in baseball, hitters are struggling now more than ever because the pitchers know the exact weaknesses of every player. In the NBA, teams are shooting more 3 point shots because of the analytics. In the NFL, teams are increasingly 'going for it' on 4th down and 2-pt conversions. 

In the National Football League, having a good coach is invaluable. More so than in other sports, NFL coaches have a tremendous impact on the game while it is being played. When calling a play, the playcaller for each team determines the starting position of the players and their responsibility for each play. On offense, the play is usually designed to gain the most yards possible. On defense, the play is usually designed to stop the offense from advancing. Coaches choose plays based off many factors, including what they anticipate the other team to do, situation of the play, score of the game, personnel, formation, previous outcomes of that playcall, randomness, injuries, and sometimes just a gut feeling. If you know what play the other team is going to run, your chances of success are a lot higher. Successful coaches are known to have 'unpredictable offenses', where there's an equally likely chance that a pass or a run is called. I want to investigate which coaches are the most predictable. 

The goal of this project is to build several classification models that predict whether an NFL team is going to pass or throw. I developed multiple models including Logistic Regression, KNearestNeighbors, Decision Tree, Bagged Decision Tree, Random Forest, AdaBoost, and Support Vector classifiers. I also developed a neural network using Tensorflow. Success will be based on accuracy, how often my model correctly predicts the play that's run. This project will be useful to anyone in the football industry that wants an edge over their opponent. It could also be helpful to bettors looking to take advantage of game props

---
## Datasets

Gathered 2020 play-calling data from http://nflsavant.com/about.php. 46,289 nfl plays from the 2020 season.
Added Defensive rankings from https://www.pro-football-reference.com/years/2020/opp.htm. 

---

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---| 
|OffenseTeam|object|nfl_plays|offensive team name|
|DefenseTeam|object|nfl_plays|defensive team name|
|ToGo|int|nfl_plays|yards until the first down|
|DefensePassRank|int|def_ranks|rank of the pass defense|
|DefenseRunRank|int|def_ranks|rank of the run defense|
|Down|int|nfl_plays|down of the play|
|Formation|object|nfl_plays|formation of the offense|

---
## Pre-Processing

Selected only pass and run plays. Selected plays that had no penalties, challenges, or extra points. Dropped columns that had to do with the result of the play, not the play call itself. Scaled the data. Factors used in modeling: down, distance, defensive team ranks, formation of the offense. Converted the down and formation variables into dummy variables.

---
## Modeling

Base-line rate is 58.96% that the play is a pass. I filtered through all 32 teams and ran several classification models: Logistic Regression, KNearestNeighbors, Decision Tree, Bagged Decision Tree, Random Forest, AdaBoost, and Support Vector classifiers. I also built a neural network model using tensorflow.

---
## Metrics

I used accuracy to compare the models. Base-line rate is .5896. Here are the models I ran and their average accuracy score for all 32 teams: Logistic Regression: .72, KNearestNeighbors: .68, Decision Tree: .66, Bagged Decision Tree: .68, Random Forest: .69, AdaBoost: .71, Support Vector: .72, neural network = .72. 

---
## Brief Summary of Analysis/Conclusions

Most predictable teams: Rams, Steelers, Jets. The Browns’ play calls were the least impacted by distance: Run less when they’re close, pass less when they’re farther away. Rams’ play calls were by far the least impacted by down: the down helpful in predicting the Rams’ play calls.Ravens exploited their opponents’ weaknesses the best: ran against bad run defenses, passed against pass defenses. Rams’ play calls were the most impacted by formation: it was easier to predict whether or not they would pass based off their formation.

---