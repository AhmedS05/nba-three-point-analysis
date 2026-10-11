# The Three-Point Era: What Actually Predicts Winning in the NBA?

## Author: Ahmed Shahzad (AhmedS05)

## Project Description:

This project examines how the NBA's shift away from mid-range shots towards three-point shooting has changed which team statistics best predict winning. I will collect data from the 1990-91 season to the most recent completed season (2025-2026) and clean it for analysis. I will use statistical analysis and various methods to test which statistics are most strongly related to win percentage and whether differences in three-point attempts between teams and across eras play a role in this. I will present these findings using various charts and an interactive dashboard to present different views. Finally, I will present my findings, discuss their limitations, and examine how external factors, such as rule changes, influenced the results.


## Project Outline:

Overall Plan - I will collect and clean the data, describe it, and test my research questions using statistical methods and tests. Then I will visualize the results and build an interactive dashboard to display my findings. Finally, I will display my conclusions and the scope/limitations of my findings. 

### Research Questions:
- How has the number of three-point attempts per game changed over time (1990-2026)?
- Do playoff and non-playoff teams differ in their three-point shooting?
- Which team statistics best predict win percentage, and does this change from era to era?

### Interface Plan:
- I will perform analysis in Jupyter notebooks so each step can be documented, explained, and rerun
- I will build an interactive dashboard using Plotly 
- Users will be able to filter by season, era (defined by me), and team to view statistics
- Charts will be labeled and clear to read/decipher

### Data Collection and Storage Plan:
- I will pull NBA statistics from NBA.com using the nba_api, covering regular season and playoffs from 1990-2026
- The fields I will be utilizing include Team, seasons, wins, losses, win percentage, three-point percentage, attempts, field-goal percentage, pace, etc.
- Raw data will go in data/raw/ then into a MySQL database, and cleaned data will be put in data/cleaned


### Data Analysis and Visualization Plan:

**Cleaning:**
- I will convert to per-game statistics so shortened seasons are comparable. 
- Check for missing values and decide how/whether to drop or fill values based on MCAR, MAR, MNAR
- Remove duplicates, standardize the format, and detect outliers using Z-score and IQR
- Group seasons by era to compare eras

**Descriptive Statistics:**
-  Compute mean, median, mode, standard deviation, and confidence intervals for key statistics and check distribution

**Statistical Tests:**
- ANOVA with Tukey test
- Two-sample t-test to compare teams (playoff vs non-playoff)
- Chi-square test 
- Correlation, simple linear regression to see which statistic best predicts win percentage
- Non-parametric test if the data distribution is not normal
- Effect sizes and p-values computed

**Visualizations:**
- Matplotlib and Seaborn for a line chart for three-point attempts over time (across seasons and eras)
- Boxplot for eras
- Scatter plot and heatmap for key statistics and to compare teams
- I will provide explanations for each chart and what it represents