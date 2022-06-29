# NBA



### NBA Avg Age For Positions
This is the average age for each position in the NBA some players play more than one position this is why there are positions that are repeated but catagorized with another position.
![PositionAge](https://i.gyazo.com/dc1ddeb84da9fb0ce241e6d067638fb3.png)


### Team Average FG Pct
This graph shows the FG Percentage for each team from 1982 - 2022. With this graph we cant really gather too much since some teams have relocated/ renamed so this will create outliers. For example KCK (Kansas City Kings) are no longer in kansas city they are the sacramento kings. Though they have the highest percentage its not fair to compare to the others who parcentage has been weighed down by playing more seasons. 
![AvgFGPct](https://i.gyazo.com/243d57be1071bf81d7b0baaedccc7003.png)

## Team Average FG Pct 2022 Season
To clear up the issues in the last graph with the outlieres here we are only comparing the teams currently in the nba for the 2022 season. For the 2022 season the 76ers were the best at shooting of all the teams. It was a close battle however with the Golden State Warriors who did go on to win the Finals this year.
![2022avgPct](https://i.gyazo.com/6861c25be93a164f75940aaabe6dfe6d.png)


## Predicting Award Share
Award Share - The formula is (award points) / (maximum number of award points). For example, in the 2002-03 MVP voting Tim Duncan had 962 points out of a possible 1190. His MVP award share is 962 / 1190 = 0.81. [Referance](https://www.basketball-reference.com/about/glossary.html)

Just using a regression to predict the award share first removing all the 0.0 values for people who were not in the running for MVP. This lowers the amount of players from 17,000 to 300. So, with less data means less value to our model providing lower scores. However, having all the players with the 0 I found was causing the model to classify someone with a .90 as not a possiblity to win the MVP. With that being said having the lower number of 300 is actually better for the model to be more consistant and accurate. Using a gridsearch to get the best params for the model found Neighbors sould be around 15, and to further get the best results using the graph below shows that 13 gives the highest training score of 70% and testing of 57%. 

Train: 0.7006405070212477\
Test: 0.5745549143825629

![testingNeighbors](https://i.gyazo.com/33c1dc4f7026b864836d4a06405b2c5d.png)