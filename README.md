# league-of-legneds
This is a project for DSC 80 at UCSD

Introduction:

Our project chooses the data of League of Legend Competitive Matches. This data contains information of players and teams from League of Legends competitive matches. The question that we are interested in is does the average game duration differ significantly between different competitive regions in tier-one professional leagues in 2022? The reader of the website should pay attention to this question because the game duration is important for implementing strategies. Understanding the difference lets people make a more effective decision toward the games. There are 149400 rows and 123 columns in this dataset, and columns that are relevant to our questions are ‘gameid’, ‘gamelength’, ‘league’. The gameid column represents the unique identifier to each game. The gamelength column represents how long the game takes. The league in which the game was played. 

Cleaning and EDA
We clean the data by only taking a specific list of leagues, since our analysis only wants the  leagues that are in tier 1. By cleaning the data, we can focus on the data that we want. It help us to analyze the information faster. 
print(tier_1[['gameid', 'gamelength', 'league']].head().to_markdown(index=False))
| gameid           |   gamelength | league   |
|:-----------------|-------------:|:---------|
| 8401-8401_game_1 |         1365 | LPL      |
| 8401-8401_game_2 |         1444 | LPL      |
| 8402-8402_game_1 |         1893 | LPL      |
| 8402-8402_game_2 |         2271 | LPL      |
| 8402-8402_game_3 |         1900 | LPL      |


This plot shows how many games in each interval of gamelength. Most of the games have a gamelength between 1500-2500, but there are still games that have a gamelength that close to zero or over 3000.
<iframe src="assets/fig1.html" width=800 height=600 frameBorder=0></iframe>

This plot shows the relationship between different leagues and their gamelength. In this plot, we can see that LPL and LCK have a gamelength that are much more than the other leagues.
<iframe src="assets/fig1.html" width=800 height=600 frameBorder=0></iframe>


Assessment of Missingness:


Hypothesis Testing:
Null Hypothesis: There is no significant difference in the average game length between tier 1 leagues in League of Legends.
Alternative hypothesis: There is a significant difference in the average game lengths between tier 1 leagues in League of Legends.
Test statistic: T-test
Significance level: 0.05
P-value: 3.1489400690188618e-24
The T test is a good choice for this question because we are comparing the means of groups. We choose 0.05 as our significant level is because we don’t have that much evidence to reject this null hypothesis. 
We see that there is a significant difference in average game duration between different regions.



