# Stock Analysis

## Overview of Project
Steve requested our consultant team to help him with developing a VBA script to analyze the performance of 12 stocks. He is mainly interested to see the volume of stock exchange as well as the return in investment so that he can provide a recommendation to his parents on which stock(s) to invest in. The data that was provided to our team included information for 12 stocks during the years of 2017 and 2018. The data included the following attributes: 

**Ticker**: This column stores data for the abbreviation of the stock of interest  
**Date**: This column provides the day where the stock exchange was active  
**Open**: This column provides the opening stock price during the day  
**High**: Provides the highest value the stock reached during the specific day  
**Low**: Provides the lowest value the stock reached during the specific day  
**Close**: Provides the closing value the stock reached during the specific day  
**Adj Close**: There was no explanation provided for this column, but it wasn't used in the analysis. The naming sugests that this is the adjusted closing price of the stock  
**Volume**: This column provides the volume of exchange  

We provided Steve the summary results and a VBA script. He later noticed that the run time of 0.5 seconds is low for the data he provided us (12 stocks) but he is anticipating to have a larger dataset with more stocks so he asked our team to refactor the code in the meantime and make it more efficient so it can handle larger dataset with less run time. Our second project with Steve started here.

## Results
The refactoring process was focused on eliminating the need to iterate through the full dataset for each ticker and instead iterate only once through the dataset to store values in arrays and present them at the end. The run time reduced significantly from about 0.5 seconds to around 0.082 seconds (~6 times faster) with the changes in code. The two screenshots below show the run time for year 2017 and 2018 using the new refactored code:

![Runtime of 2017](https://github.com/HoussamGhandour/stock-analysis/blob/main/Resources/2017RefactoredRunTime.PNG)
![Runtime of 2017](https://github.com/HoussamGhandour/stock-analysis/blob/main/Resources/2018RefactoredRunTime.PNG)

## Summary

### What are some advantages and disadvantages of refactoring code in general?
**Advantages:**  
1. Makes the code clean and organized
2. Makes the code more efficient to run
3. Improves the design of the code
4. Improves the skillset of the coder  

**Disadvantages:**
1. Problems may arise if refactoring somebody's code without appropriate understanding of the code
2. Requires additional time and budget before delivering to the client
3. May not yield accurate results without proper testing especially when original code is not completely comprehended

### What are some advantages and disadvantages of the original and refactored VBA script?
Both codes still required data to be sorted in order of ticker name and date. The current code can't provide accurate results if the data was received in random order. It is recommended to add lines of code to sort the data prior to analysis. The refactored code is more efficient than the original code as it required less run time. In the other hand, the original code may seem to be easier to understand for public viewers.
