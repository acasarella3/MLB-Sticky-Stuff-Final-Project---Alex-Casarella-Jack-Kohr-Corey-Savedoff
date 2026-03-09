# MLB "Sticky Stuff" Final Project: Alex Casarella, Jack Kohr, Corey Savedoff

Introduction:
For our final project, we decided to expand upon the "Sticky Stuff" analysis we conducted for our midterm.

On a high-level, our midterm consisted of an analysis of baseline MLB pitcher statistics following the ban on foreign substances implemented on June 21st, 2021. In our midterm, we retrieved all MLB pitcher statistics from the MLB Stats API, subsequently using ERA, WHIP, K%, BB%, BAA, HR/9, and IP within our analysis. Then, we implemented an innings threshold to ensure sample size validity and feature engineered different time periods within our data. In addition, we queried injury data from the MLB Stats API to implement a control for significant injury status; injuries have shown to have a detrimental impact on pitcher performance.

When our data set was analysis ready, we conducted a variety of Python EDA's: line plots, KDE's, histograms, bar charts, annotated scatter plots, and correlation heatmaps. Furthermore, we conducted paired and two-sample t-tests to derive the statistical signifcance of performance shfits. Lastly, we isolated pitchers by largest decreases in ERA and K% to see who was most affected by the ban.

To deepen our analysis for the final project, we used pybaseball to retrieved hundreds of thousands of pitches and their respective movement from Baseball savant. This was the logical progression as "sticky stuff" has a direct impact on ball flight and movement; actual pitcher statistical performance is solely a downstream effect of the crackdown, while ball movement is the mechanism. We then loaded all three databases (MLB pithcer statisitcs, injury data, and pitch movement) into a SQLite database for SQL analysis.

After our data set was analysis ready, we used aggregate tables to see the spin rate data for different time periods, injured & non-injured groups, and general largest movers. We then conducted a varity of Python EDA's to further evaluate the data: histograms, KDE's, and pair plots. Furthermore, we built a linear regression model to predict each pitcher's K% change (pre to post crackdown) using Statcast features, traditional stats, and our engineered variables. We also built a logistic regression model to classify pitchers as "significantly affected" or not (pitchers whose K% decline was greater than the median decline across all qualified pitchers.)

Overall, our analysis was aimed at analyzing our four key questions:
1. Did league-wide strikeout rates and pitching dominance decline after the crackdown?
2. Which individual pitchers showed the largest performance drops, and do those names match the public narrative?
3. Are the observed changes statistically significant, even after controlling for injuries and aging?
4. Does Statcast spin rate data confirm the mechanism — did pitchers actually lose spin after enforcement?
