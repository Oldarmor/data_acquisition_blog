# README
## Introduction
This repo includes the code used to pull and create the data set used in my Golf Analysis blog. The numbers were pulled from the pgatour.com website, and merged the different datasets together to create a specific dataset that only includes the data I'm interested in. All the data is from the 2025 pga tour season up through the World Wide Technology Championship on November 9th.
### The CSV's
In this repository there are several difference CSV's. The 'golf_data.csv' represents the final data frame that is made after merging and cleaning the data. The other CSV's (in the input folder) include certain data regarding different players putting, green in regulation, fairways hit, etc.. I was mostly interested in the statistics recorded, like putts per round, or green in regulation percentage, but the individual CSV's contain more data like total putts, total rounds, and others.
### The Notebook
The 'data_acquisition.ipynb' is the jupyter notebook that includes the code used to merge all the data together and clean it to prepare it for analysis. I used a for loop to look through each individual CSV and pull the column of interest out, and merge that into the data frame.
### Data Overview/Dictionary
Overall we finished with 8 columns and 177 rows. Below is a dictionary defining each column name, what it means, and the data type in the column. 
PLAYER_ID - the individual player id of each player in the data set. (int) 
PLAYER - The name of the individual player. (string) 
AVG - That players scoring average per 18 holes for the current season. (float) 
driving_distance_AVG - the average driving distance of that player. Note each tournament only has 2 out of the 18 holes that measure this. (float) 
fir_% - Percentage of fairways hit in regulation, regardless of club used off the tee. Fairway in regulation means you hit the fair way with your first shot on non par 3 holes. (float) 
gir_% - Percentage of greens hit in regulation. A green in regulation is counted if you are on the green with at least 2 shots away from par. (float) 
putting_AVG - Average total number of putts per 18 holes recorded by that player. A putt is a shot hit with the putter while on the green. (float) 
scrambling_% - A percent value of how often a player successfully scrambles. A scrambling opportunity is only recorded when a player is not on a green in regulation, and a success means that the player was not on the green in regulation but still recorded par or better. (float) 
