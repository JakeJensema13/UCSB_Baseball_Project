UCSB_Baseball_Project_Report_NoCode.html - Final report with no code blocks

UCSB_Baseball_Project_Report_Code.html - Final report with code blocks

# Introduction
In the fall of 2023, I had the exciting opportunity to join the UC Santa Barbara Baseball Analytics Team as a research analyst. Collaborating with fellow UCSB students, my role involved diving deep into the world of baseball analytics. During the 10-week fall quarter, we embarked on an independent research project, which led me to explore Trumedia, an extensive online database featuring a wealth of college baseball statistics and advanced metrics.

While analyzing our team's data, I noticed an intriguing discrepancy: the Expected Batting Average (xAVG) of our players was significantly lower than their actual batting averages. xAVG, a metric predicting the likelihood of a batted ball becoming a hit, intrigued me. On Trumedia, xAVG is calculated based on two primary factors:


**Launch Angle:** The angle the ball comes off of the ball when hit into play

**Exit Velocity:** The exit velocity in mph the ball comes off of the bat

This straightforward calculation, relying solely on exit velocity and launch angle, appeared overly simplistic at first glance. It is true in baseball that a ball hit with a higher exit velocity is generally more challenging to field due to the decreased reaction time. The formula used for the MLB xAVG seems to perform well but the MLB uses sprint speed as a factor which is not available to me on Trumedia. This led me to delve deeper into the nuances of these statistics and their implications in baseball analytics.

# My Solution
While I still acknowledge the significance of exit velocity and launch angle in baseball analytics, I believe there's a broader narrative to uncover. To expand our understanding, I introduced a novel variable named **pCallStrike%**. This metric estimates the likelihood that a pitch would have been called a strike had the batter not swung. Including this allows us to integrate pitch location into our new metric, crucial since hitting a ball thrown down the middle is easier than one on the edge of the strike zone.

Further refining our analysis, I created a classification system named **Good Pitch.** This system assesses each pitch, categorizing it as bad, good, or great based on key metrics like vertical break, spin rate, and velocity.
From here I employed an array of classification models to give every pitch a probability of being predicted as a hit. My best model which was a gradient boosted tree had a 75% accuracy rate.

# Evaluation
After conducting a thorough evaluation of my newly developed xAVG metric in comparison to our previous standard, it became evident that xAVG significantly outperforms the old metric, which consistently undervalued nearly every player. This revelation prompted me to present my findings to the coaching staff. They showed a keen interest and expressed a desire to explore how we can effectively incorporate my model into our strategy for the upcoming baseball season, which commences this spring.
