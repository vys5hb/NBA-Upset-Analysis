# NBA Upset Analysis
By: Ethan Ooi

NBA Upset Analysis is a model created to analyze key factors that influence underdog wins. An underdog is a team which has a Vegas betting spread greater than 0, this implies that the team is an underdog to win the game. An upset is defined by an underdog team winning their respective game. The results are pulled from data from NBA Regular and Post-Season games from the 2007-08 eason to the 2017-18 season. The factors used are a team's winning percentage (`w_pct`) and a team's home-court advantage (`is_home`). A team's win percentage was used by categorizing a team into four separate bins. Low, Mid-Low, Mid-High, and High. These categories mean that a team's win percentage is in the bottom 25th percentile, 25-50th percentile, 50-75th percentile, and top 25th percentile, respectively. This repository contains all the code for the project in __NBA_Database.ipynb__, as well as the csv files in __nba_data__. 
The folder __created_datasets__ contains any csv files created in __NBA_Database.ipynb__.

# Methodology
My data was obtained using *NBA Historical Stats and Betting Data* from Kaggle. This dataset can be found in the GitHub under __nba-historical-stats-and-betting-data.zip__. For this project, I only needed two datasets which can be found in __nba_data__. I took this dataset and cleaned it of unnecessary variables like player stats and game stats as you would not know these stats before the game happened. Discussed before, I used Vegas betting spreads where a positive spread is an underdog and a negative spread is a favorite. Using the data of betting spreads from a separate dataset, I merged the two datasets found in __nba_data__ on `game_id` and created a new variable, `is_upset`, where the team with a `spread1` > 0 and a win would be an upset.

# Results
The overall upset rate was 49.10%.


Underdog teams playing away win 28.20% of the time, while underdog teams playing at home win 70.79% of the time. 
This can be attributed to many factors such as crowd pressure, players being comfortable at home, and travel.
![image](https://github.com/user-attachments/assets/b6e9d80f-9009-49b5-a047-101212e19c4c)
![image](https://github.com/user-attachments/assets/a6baa62b-00e8-42fb-987d-6f584d8878b6)


Underdog teams in the bottom 25th percentile of win percentage win 26.74% of the time, while underdog teams in the top 25th percentile win 69.12% of the time. We see a continual increase in win percentage as we increase win percentage. This makes sense as teams with a higher win percentage are better teams and in the occurence where they are underdogs, their win percentage as underdogs is very high.
![image](https://github.com/user-attachments/assets/9d8f6950-96fb-4eed-b522-ca679c778f3a)
![image](https://github.com/user-attachments/assets/d533ecc2-c61a-4203-9ce1-a0cdd651205f)


Underdog teams playing at home in the top 25th percentile win 81.05% of the time, while underdog teams playing at home in the bottom 25th percetile win only 50.57% of the time. Underdog teams playing away in the top 25th percentile win 42.13% of the time, while underdog teams playing away in the bottom 25th percentile win 18.23% of the time. I view these results as very shocking, even the best underdog teams playing away win less often than the worst underdog teams playing at home. 
![image](https://github.com/user-attachments/assets/4369d07e-3da0-4ca2-a13d-998ee2839a96)
![image](https://github.com/user-attachments/assets/122c83ba-af89-451a-9f13-08f1fc1f368d)



# Discussion + Conclusion
It shows that both team win percentage and home-court advantage plays a huge role in whether a team will pull off an upset. One take-away from this is if you were to bet a flat amount on every underdog team that played at home, statistically you would be making profit in the long run. Especially since underdogs pay out minimum of 2x your bet and tend to be around 2.5-3.5x of your bet. And, the overall upset rate being so close to 50%, does this mean that in a large sample size, there truly is no difference when picking teams to win if over so many games, underdogs win 49.10% of the time.