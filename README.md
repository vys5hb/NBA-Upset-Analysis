By: Ethan Ooi

I created this project to analyze different factors that may cause upsets in NBA games. 
The results are pulled from NBA Regular and Post-Season games from the 2007-08 season to the 2017-18 season.
The factors used are a team's winning percentage (w_pct) and a team's home-court advantage (is_home).
I use Vegas betting spreads to determine an upset. An upset is defined by a team whose Vegas betting spread is > 0, and they win.

There are various results that lead to interesting findings like:

Underdog teams playing away win 28.20% of the time, while underdog teams playing at home win 70.79% of the time.

Underdog teams in the bottom 25th percentile of win percentage win 26.74% of the time, while underdog teams in the top 25th percentile win 69.12% of the time.

Underdog teams playing at home in the top 25th percentile win 81.05% of the time, while underdog teams playing at home in the bottom 25th percetile win only 26.74% of the time.

Underdog teams playing away in the top 25th percentile win 42.13% of the time, while underdog teams playing away in the bottom 25th percentile win 50.57% of the time.

This repository contains all the code for the project in NBA_Database.ipynb, as well as the csv files in nba_data. 
The folder created_datasets contains any csv files created in NBA_Database.ipynb

