# Week 3

**Dates:** 07-06 to 07-10

## Goals

- Make the following suggested changes to my CNN pipeline and journals:

- First, check the ORACLE dataset parsing carefully. The ORACLE documentation notes that the data may need to be parsed as complex128, even if the metadata suggests cf32/complex64. If the binary files are read with the wrong dtype, the samples can be corrupted. Please confirm this, update the converter if needed, and document the choice in the dataset README.

- Second, make sure the CNN training script is actually training on ORACLE data, not the synthetic toy data. Some of the current scripts and folder names make it a little hard to tell which dataset is being used. Please create a clear ORACLE training command, for example something like this: "python -m src.training.train --config configs/oracle_cnn.yaml" That config should specify the ORACLE dataset path, window length, channels, normalization, split, model, batch size, learning rate, seed, and output folder.

- Third, work on the split protocol. A random window-level split is okay for debugging, but it can overstate RF fingerprinting performance, especially if adjacent or overlapping windows from the same recording appear in both train and test. For the next result, please save an explicit split file and include enough metadata to check for leakage. Each window should keep metadata such as device ID, source file, run/configuration, window start/end, dataset name, and any available ORACLE condition labels.

- Fourth, every reported run should save the basic research artifacts. At minimum, please save:

    config.yaml
    metrics.json
    confusion_matrix.png
    confusion_matrix.csv
    training_curves.png
    split file or split hash
    random seed
    git commit hash
    Also include accuracy and macro-F1, not accuracy alone. Macro-F1 is important because it tells us whether the model is working across classes rather than doing well only on easier or more frequent classes.

- Fifth, please try to update your weekly research log using a standard format. A good template is:

    Week:
    Goal for this week:
    What I completed:
    Best run ID and git commit:
    Dataset and split:
    Window length and channels:
    Model:
    Metrics:
    Confusion matrix file:
    What failed or looked suspicious:
    What I will do next:
    Question for supervisor:

## Approach and Implementation

- I will look at the suggested changes then implement them into my code.

- The ORACLE parsing has been verified and implemented; it will prefer complex128 to avoid sample corruption

## Results

- So far, I have fixed the ORACLE dataset parsing to prefer compllex 128.
- I have also completed the YAML config files.
- I must work on the split protocol next week.

## Notes

- Working with YAML files has been a bit easier than expected.
- I wonder why I am still getting 100% training accuracy still with minimal loss.