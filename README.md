# Refactoring Stock Analysis Code

## Overview of Project

### Purpose and Background
Steve requested an analysis of different stocks to provide research to his family. This was provided with buttons to allow him to run
the analysis as he wished. However, because this analysis ran over a contained set of data points, I wanted to refactor the code to make
sure that if a larger data set were analyzed, it could be done in a reasonable amount of time. This also required making sure that the
original functionality of the code (allowing Steve to choose what year he wanted analyzed) to stay intact.
## Results
Steve's goal was to look at  the return percentage on the stock DQ. Based off the code that I wrote, in 2017 DQ was up 199.4%. However,
looking at DQ's return in 2018, it showed it at -62.6%. Looking at the other stocks that Steve provided, ENPH and RUN were the only two
that posted a gain on return in both 2017 and 2018, with ENPH increasing 199.4% in 2017 and 81.9% in 2018 and RUN increasing 5.5% in 2017 and 84.0% in 2018. Running my original code for 2017 took 0.34375 seconds, while running it for 2018 took 0.3515625 seconds. 
