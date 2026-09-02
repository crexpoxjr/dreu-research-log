# Week 7

**Dates:** 08-03 to 08-07

## Goals

- Fully adapt WiSig dataset.

- Implement a robustness suite.

## Approach and Implementation

- I will first implement the WiSig dataset into the pipeline

- I will measure the results of the WiSig dataset to that of the ORACLE subset

- The WiSig website contains 4 datasets, but I will use ManySig.pkl and Single-Day.pkl 

## Results

- Using the Single-Day.pkl, I achieved an accuracy closer to using ORACLE, around 20-30%

- However, using the ManySig.pkl file in the pipeline, the accuracy shot up to around 80%

## Notes

- I am not sure why the accuracy has increased drastically using the ManySig data, though I theorize it has to do with how my pipeline handles sigmf data, and how ManySig files are in the .pkl file. Since the model has more data to train with, it will perform better.