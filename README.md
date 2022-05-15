# Stocks Analysis

## Overview of Project

### Purpose
The client, Steve, wishes to help his parents diversify their stock portfolio in various other green energy companies besides DAQO New Energy Corp (DQ). This analysis should provide further insight on which stocks appear to be worth the risk investing in and which ones are not.

## Results

### Stock Performance - 2017 VS 2018
![2017](/Resources/2017_Summary.PNG) ![2018](/Resources/2018_Summary.PNG)

While most stocks saw net positive returns in 2017, most stocks also saw net negative returns in 2018. The only two stocks that continued to see a net increase were ENPH and RUN. ENPH was the third best performing stock in 2017 and the second best performing stock in 2018, suggesting it has a more stable growth pattern than the other stocks. RUN, on the other hand, was the 11th best performing stock in 2017 (with only a 5.5% net return) and the top performing stock in 2018. This stock may be worth investing in, but doing a deeper investigation into why the growth was so slow in 2017 may help determine whether that would be worth doing (perhaps a big change occurred in the company).

### VBA Performance
Originally, this script performed around 1 (0.945) second each time it ran. The core structure within the script looped through the raw yearly data one time for each stock, meaning it looped a total of 12 times. With the current dataset, it is by no means slow, but the addition of more stocks to analyze may cause the script to run longer and more ineffecient. 

To correct this, the script was refactored to loop through the data once and instead store values within arrays that updated based on the current stock being analyzed. It is important to note, however, that this is dependent on the data first being organized by stock name and date prior to running the script. 
Below are the new times that the script ran in, proving to be much more effecient and scalable.

![2017_time](/Resources/VBA_Challenge_2017.PNG)
![2018_time](/Resources/VBA_Challenge_2018.PNG)

### Limitations
It may be worth allowing for analysis between longer ranges of time, for example between the start of 2017 and the end of 2018. Despite the fact that most stocks did not perform as well in 2018, a few of them may still have had net positive returns during that 2-year period. Also, because not all stocks are worth the same value, a 5% gain or loss in one stock may not have the same ramifications as a 5% gain or loss in another stock.

## Summary

Refactoring code may not always be needed, specificaly in circumstances where datasets are tiny (making any benefits received from refactoring very minimal) or where the time needed to complete a refactor outweighs the total time one might spend running the analysis as is.

The dataset used in this analysis was quite small, so the difference between 1/10th of a second and 9/10ths of a second don't justify the need for refactoring as it exists now.