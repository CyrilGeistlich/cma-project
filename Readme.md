# Proposal for Semester Project

**Patterns & Trends in Environmental Data / Computational Movement
Analysis Geo 880**

| Semester:      | FS23                                     |
|:---------------|:---------------------------------------- |
| **Data:**      | Movement data (Posmo Project)            |
| **Title:**     | "Automated Transportation Mode Differentiation using GPS Tracking Data: Exploring Factors, Features, and Machine Learning Approaches"                              |
| **Student 1:** | Cyril Geistlich                          |
| **Student 2:** | Micha Franz                              |

## Abstract 
<!-- (50-60 words) -->

This project aims to investigate key factors and features in GPS tracking data to differentiate transportation vehicles. Machine learning is applied to automate transportation mode detection using spatial, temporal, and attribute analysis. Manual verification of results ensures accuracy. The findings contribute to computational movement analysis and automated transportation mode detection.

## Research Questions
<!-- (50-60 words) -->

What are the key factors and features that can be extracted from GPS tracking data to differentiate between different types of transportation modes?
How can machine learning techniques be applied to GPS tracking data to automate the detection of the mode of transportation and which accuracies can be achieved by different machine learning algorithms?


## Results / products
<!-- What do you expect, anticipate? -->

We expect to define the principle components contributing to the identifiaction of unique transportation modes. With this insight we hope to train a machine learning model which can accurately extract the mode of transportation from GPS movement data. We expect different machine learning techniques to yield varying accuracies.  

## Data
<!-- What data will you use? Will you require additional context data? Where do you get this data from? Do you already have all the data? -->

The main data set is tracking data gathered by the Posmo Project. The data includes GPS position and automatically assigned labels corresponding to the mode of movement. The Posmo Project is available as a downloadable smartphone application and reads the GPS position for the user with sampling intervals of 5 to 10 seconds. Ideally, we retrieve continuous data, but we expect there to be varying sampling rates throughout the data set.


## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using? -->

<<<<<<< HEAD

=======
We will try to deduce as many parameters from the GPS tracking data as possible, such as velocity, acceleration, trip duration, turning angle, slope, time and position .We then want to conduct a principle componenet analysis to find the components which contribute to 90% of the variability. We then will use these principal componenets to train our model. We will evaluate different methods using accuracy measures such as recall, precision and F1-Score. We will apply k-fold cross validation.
>>>>>>> 0b0498ce24b7e3a9ba85d88de124da42f0fc7b43

## R concepts
<!-- Which R concepts, functions, packages will you mainly use. What additional spatial analysis methods will you be using? -->

We will use R base funcitonalities to manipulate and prepare our data. The library "dplyr" will certainly be used with its mutate, select and filter functions. 
To implement the machine learning algorithms we will use multiple libraries. Namely cluster, class, Rtsne, randomForest, rpart, neuralnet and caret.
To evalaute the machine learning results we will use MLmetrics
We will use ggplot2 and the "sf" library for data visualization. 

## Risk analysis
<!-- What could be the biggest challenges/problems you might face? What is your plan B? -->

Labeling Ground Truth: Manually labeling segments with the actual mode of transportation for verification can be time-consuming and might lead to errors or inconsistencies.
Class Imbalance: The frequency of different transportation modes in the GPS tracking data may vary quite a bit, leading to class imbalance issues. This can affect the training and evaluation of machine learning models, potentially biasing the results towards the prevalent classes.
GPS Inaccuracy & Noise: Factors such as tall buildings, tunnels, or being inside trains can affect GPS signals, leading to noise and inconsistencies in the data. Accounting for these factors in the analysis and modeling process can be challenging.

If the machine learning approach turns out to be to complex/time consuming we would implement rule-based algorithms or heuristics to differentiate between transportation modes. This rule-based approach would rely on predefined rules and thresholds based on theory knowledge or domain-specific guidelines to classify the transportation modes. While it may require more manual work and customization, it offers more transparent and easier to understand.

## Questions? 
<!-- Which questions would you like to discuss at the coaching session? -->
Is it realist for us to implement a machine learning algorithm in this course or would it be better to apply other methods to classify the mode of transportation?
