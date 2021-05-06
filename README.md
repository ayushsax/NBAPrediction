# NBAPrediction

## Model
The model uses five factors scraped from stats.nba.com to determine the predicted result of an NBA game.
1. Field Goal Percentage
2. Free Throw Percentage
3. Rebounds
4. True Shooting Percentage
5. Three Point Percentage


To approximate spreads and game totals, the python notebook uses ridge regression and linear regression, respectively. It is able to predict more than 60% of the games correctly, which is enough to make a profit while betting on basketball. 

You may run the notebook [here](https://drive.google.com/file/d/1_5jTvIv0cp0m409S010UiOXfgTYYhIs1/view?usp=sharing) with Colab, or look at the installation steps.

## Installation
1. Download the ZIP files for this repository
1. Copy the main repository link for NBAPrediction (https://github.com/ayushsax/NBAPrediction)
2. Go to [Google Colab](https://colab.research.google.com/) and go to the Github tab
3. Paste the URL in the top text bar
4. Upload all of the the .csv files from the ZIP file inside the main folder in the files tab (left side)
5. Select Runtime - Run All to run the notebook

Note: You may also run this notebook locally but Google Colab is recommened.

## Usage
The prediction model is under the UI section in the notebook. You can find this section in the table of contents or at the bottom of the notebook. After you run all of the cells in the notebook, the UI will appear with a menu with some options.

Here are the descriptions of the options:
1.  1 NBA Team: Team match-up between 2 NBA teams. There are 2 selection menus where you can set home and away teams.
2.  Random Simulation: Runs a random simulation where for each simulated game, two random teams are chosen to play against each other. There is an extra parameter to determine the count of games to simulate.
3.  2018-2019 Season: Simulates games from the 2018-2019 season schedule using the exact teams in the NBA dataset from that time period
4.  2020-21 Season: Simulates games from May 2021 NBA season schedule in purpose for predicting future games
There is another parameter, alpha, which represents the scalar value of the performance gains/losses for each team based on each game. The features that are listed above in the document would vary for each team depending whether they win/loss for each game. For instance, if a home team wins, all values of their point types would increase by multiples of alpha; therefore, their values of each feature will increase and would have a higher chance of winning.

## Output
After running the simulation, the Summary tab will appear containing the average winning percentages and average spread for all home teams in the simulation. On the top right, there is a bar graph displaying the winning percentages for each home team for comparisons. Each tab contains all games for each team in the simulation. For each game, it displays the matchups, spreads, total points, and the gains/losses for each point type that would be influenced in later games.
