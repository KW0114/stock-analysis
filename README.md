# Studying Effects of Refactoring Code

## Overview/Purpose
This analysis was to revisit the solution to a problem for the purpose of making the code more efficient and reducing runtime. 

### Results

The initial analysis was run on a dataset of stocks to find the total daily volume and return percent for each type of stock. 
Originally, the code looped through the entire dataset several times with nested for loops, which made the runtime pretty 
slow:

![code screenshot](https://github.com/KW0114/stock-analysis/blob/bf297618d090d83e4f187d6d31a301ecb0f8d163/Original_Loops.png)

There were over 3000 entries in this dataset, so you can imagine how long it took to loop through every element so many times!
When I refactored the code, I just wrote one single for loop that did each check only once as we looped through the dataset:

![code screenshot](https://github.com/KW0114/stock-analysis/blob/7b438ea954e19b2c9dc332346dbabba31a7702bc/Refactored_Code.png)

#### Original Runtimes
The original code ran in almost .7 seconds. Before the changes, here are the new runtimes for each year:

![runtime screenshot](https://github.com/KW0114/stock-analysis/blob/10ac863e6a01bace744d55ee9ec852ca6a5a8c10/Original_2017.png)

![runtime screenshot](https://github.com/KW0114/stock-analysis/blob/10ac863e6a01bace744d55ee9ec852ca6a5a8c10/Original_2018.png)

#### Refactored Runtimes
After the changes, here are the new runtimes:

![runtime screenshot](https://github.com/KW0114/stock-analysis/blob/7b438ea954e19b2c9dc332346dbabba31a7702bc/VBA_Challenge_2017.png)

![runtime screenshot](https://github.com/KW0114/stock-analysis/blob/7b438ea954e19b2c9dc332346dbabba31a7702bc/VBA_Challenge_2018.png)

## Summary
* The biggest advantage of refactoring code is achieving a shorter runtime.
* Many times, revisiting old code makes it much easier to see a more sophisticated way of solving the same problem.
  * The only disadvantage I could see would be if you came up with an efficient solution the first time, and basically
  you would just be wasting extra time trying to refine it for no reason.
* Looking at the code for this project, it was definitely worth revisiting. This is a relatively small dataset, and having nested loops
can create an exponential effect on runtime. The bigger the input, the more noticeable the lag in runtime would be.


