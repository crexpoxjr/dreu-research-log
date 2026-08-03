# Week 4

**Dates:** 07-13 to 07-17

## Goals

- Continue and finish working on suggested changes.

- Discover why there is 100% training accuracy.

- Finish pipeline with a realistic and satisfactory accuracy.

## Approach and Implementation

- I have discovered that the dataset I am using is from only one device, as such I downloaded the first dataset from the list of ORACLE datasets, which contains data from 16 devices.

- This datset was too big for my pipeline, so I had to trim down the dataset and set a limit on the window size and class count so my system would not run out of memory and crash.

- I adapted the CNN to use this new dataset. I also added configs to tweak things like the window size/length, max classes, and 



## Results

- I achieved around a 6% accuracy rate wth 8 classes, and it looks like there are cluster-like concentrations around some classifications.

-I tested the CNN with smaller window sizes over 500 epochs, the results seem to suggest that there may be an issue regarding the data, probably through the regularization process.


## Notes

-I need to find some way to fix the normalization process.

