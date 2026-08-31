# Week 6

**Dates:** 07-27 to 07-31

## Goals

- Fix data conversion.

- Work on multi-channel CNN.

- Try and find the reason for low accuracy rates.

## Approach and Implementation

- I will run two main tests with two different configs: one where small windows are organized into two classes over 500 epochs, and another one where bigger windows are organized into 8 classes over 40 epochs. I hope these two tests will give me more insight into what is happening in my pipeline.

- I will also inspect the recorded metrics for each run, for example things like the confusion matrices and f1 scores.

- Additionally, I will also adpat the WiSig dataset into the pipeline to see if there are any differences between the processing and training of both datasets.

## Results

- Using the training accuracy data, I can see that the model tends to favor some class specifications over others while still achieving a high training accuracy. This might suggest the model is memorizing the dataset rather than learning from it.

## Notes

- I will try implementing the WiSig dataset into then pipeline to see if that will give me further insight into how to fix the CNN

