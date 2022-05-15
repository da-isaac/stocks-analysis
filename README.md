# Stocks Analysis

## Overview of Project

### Purpose
The client, Steve, wishes to help his parents diversify their stock portfolio in various other green energy companies besides DAQO New Energy Corp (DQ). This analysis should provide further insight on which stocks appear to be worth the risk investing in and which ones are not.

## Results

### Stock Performance - 2017 VS 2018
![2017](/Resources/2017_Summary.PNG) ![2018](/Resources/2018_Summary.PNG)

While most stocks saw net positive returns in 2017, most stocks also saw net negative returns in 2018. The only two stocks that continued to see a net increase were ENPH and RUN. ENPH was the third best performing stock in 2017 and the second best performing stock in 2018, suggesting a steadier growth than the other stocks. RUN, on the other hand, was 11th best performing stock in 2017 (with only a 5.5% net return) and the top performing stock in 2018, suggesting it may still be a riskier investment.

### VBA Performance
Originally, this script performed around 1 (0.945) second each time it ran. The core structure within the script looped one time for each stock, meaning it looped a total of 12 times through the year data. It is by no means running slow currently, but the addition of more stocks to analyze (and subsequent lengthening of the raw data because of that addition) may cause the script to get increasingly long and ineffecient. 

To correct this, the script was updated to only loop through the data once and instead store values within arrays that updated based on the current stocks being analyzed. It is important to note, however, that this is dependent on the data being organized by stock and date prior to running the script. Below are the new times that the script ran in, proving to be much more effecient and scalable.

![2017_time](/Resources/VBA_Challenge_2017.PNG)
![2018_time](/Resources/VBA_Challenge_2018.PNG)

### Limitations
It may be worth allowing analysis between longer ranges of time, for example between the start of 2017 and the end of 2018. Despite the fact that most stocks did not perform as well in 2018, a few of them may not have lost as much value as is needed to completely eliminate them from consideration. Also, because not all stocks are worth the same value, a 5% gain or loss in one stock may not have the same ramifications as a 5% gain or loss in another stock.

## Summary

Refactoring code is useful in situations where datasets are either large or could grow larger with time, but it may not always be useful or necessary if the datasets are not large. 


The run time before and after refactoring of this project do not justify the time spent doing it, unless the datset considers more stocks each year in the future.