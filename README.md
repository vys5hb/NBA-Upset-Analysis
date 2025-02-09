# NBA Upset Analysis
By: Ethan Ooi

NBA Upset Analysis is a model created to analyze key factors that influence underdog wins. An underdog is a team which has a Vegas betting spread greater than 0, this implies that the team is an underdog to win the game. An upset is defined by an underdog team winning their respective game. The results are pulled from data from NBA Regular and Post-Season games from the 2007-08 eason to the 2017-18 season. The factors used are a team's winning percentage (w_pct) and a team's home-court advantage (is_home). A team's win percentage was used by categorizing a team into four separate bins. Low, Mid-Low, Mid-High, and High. These categories mean that a team's win percentage is in the bottom 25th percentile, 25-50th percentile, 50-75th percentile, and top 25th percentile, respectively. 

# Methodology
My data was obtained using *NBA Historical Stats and Betting Data* from Kaggle. This dataset can be found in the GitHub under nba-historical-stats-and-betting-data.zip. For this project, I only needed two datasets which can be found in nba_data. I took this dataset and cleaned it of unnecessary variables like player stats and game stats as you would not know these stats before the game happened. Discussed before, I used Vegas betting spreads where a positive spread is an underdog and a negative spread is a favorite. Using the data of betting spreads from a separate dataset, I merged the two datasets found in nba_data on game_id and created a new variable, is_upset, where the team with a spread1 > 0 and a win would be an upset.

# Results
The overall upset rate was 49.10%.


Underdog teams playing away win 28.20% of the time, while underdog teams playing at home win 70.79% of the time. This can be attributed to many factors such as crowd pressure, players being comfortable at home, and travel.
![alt text](image-24.png)                  
![alt text](image-27.png)


Underdog teams in the bottom 25th percentile of win percentage win 26.74% of the time, while underdog teams in the top 25th percentile win 69.12% of the time. We see a continual increase in win percentage as we increase win percentage. This makes sense as teams with a higher win percentage are better teams and in the occurence where they are underdogs, their win percentage as underdogs is very high.
![alt text](image-25.png) 
![alt text](image-28.png)


Underdog teams playing at home in the top 25th percentile win 81.05% of the time, while underdog teams playing at home in the bottom 25th percetile win only 50.57% of the time. Underdog teams playing away in the top 25th percentile win 42.13% of the time, while underdog teams playing away in the bottom 25th percentile win 18.23% of the time. I view these results as very shocking, even the best underdog teams playing away win less often than the worst underdog teams playing at home. 
![alt text](image-26.png) 
![alt text](image-29.png)


# Discussion + Conclusion
It shows that both team win percentage and home-court advantage plays a huge role in whether a team will pull off an upset. One take-away from this is if you were to bet a flat amount on every underdog team that played at home, statistically you would be making profit in the long run. Especially since underdogs pay out minimum of 2x your bet and tend to be around 2.5-3.5x of your bet. And, the overall upset rate being so close to 50%, does this mean that in a large sample size, there truly is no difference when picking teams to win if over so many games, underdogs win 49.10% of the time.