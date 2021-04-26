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

![2017_Original](https://github.com/swlim314/Stock-Analysis-Week-2/blob/f1f22e6bb862cb403039bac743d3d1f9fc71bec6/VBA_Challenge_2017_original.png)

![2018_Original](https://github.com/swlim314/Stock-Analysis-Week-2/blob/f1f22e6bb862cb403039bac743d3d1f9fc71bec6/VBA_Challenge_2018_original.png)
The new code required additional arrays to deal with stock volume, Starting prices, and Ending prices. Those were added in my code as 
**Dim tickerVolumes(12) As Long**
**Dim tickerStartingPrices(12) As Single**
**Dim tickerEndingPrices(12) As Single**
The variable tickerIndex was also intiated to use to call out the specific index of each of those arrays. With the code updated with
additional arrays, and using for loops, the time to analyze 2017 stocks went down to 0.0625 seconds, and the time to analyze 2018 stocks also took 0.0625 seconds.
![2017_Refactored](https://github.com/swlim314/Stock-Analysis-Week-2/blob/f1f22e6bb862cb403039bac743d3d1f9fc71bec6/VBA_Challenge_2017.png)
![2018_Refactored](https://github.com/swlim314/Stock-Analysis-Week-2/blob/f1f22e6bb862cb403039bac743d3d1f9fc71bec6/VBA_Challenge_2018.png)

## Summary

### Advantages and Disadvantages of Refactoring
In general, refactoring code allows me to run larger data sets in a more reasonable amount of time. It also keeps the data stored
properly in arrays versus having to keep specifying cells that could be moved around or edited. However, refactoring code also requires
more troubleshooting to make sure everything works correctly. There is additional time spent making sure that there are no errors in
coding, which depending on the data being analyzed might not be worth spending the time on.

### Advantages and Disadvantages of Original code vs Refactored code
By refactoring the code, I was able to drop the run time by 5.5 times for the 2017 analysis, and 5.63 times for the 2018 analysis.
This means that in the future, Steve will be able to run data sets several times larger within a reasonable amount of time. However,
refactoring the code involved additional troubleshooting to make sure all the values were still working. By adding more arrays, there
were more moving parts that needed to be kept track of. The original code only used one array, and due to that had fewer lines of code. Although it was slower in its run time and not well suite for large data sets, it didn't require as many call backs to arrays and value sets.

## References
For the Module 2 challenge, **chkCreate** helped me work through the logic of the code.
