# Exercise 3 - Kaggle competition

This exercise is in the form of a Kaggle competition. A few quick details on Kaggle & the competition format:

- Kaggle (https://en.wikipedia.org/wiki/Kaggle) is a platform that allows a competition for a certain data set. Participants submit their prediction on a test set, and will get automated scoring on their results, and will enter the leaderboard.
- From Kaggle, you will be able to obtain a labelled training set, and an unlabelled test set.
- You can submit multiple entries to Kaggle; for each entry, you need to provide details on how you achieved the results - which software and which version of the software, which operating system, which algorithms, and which parameter settings for these algorithms; further, any processing applied to the data before training/predicting. There is a specific "description" field when submitting, you should fill in this information there, and you also need to include this description and the actual submission file in your final submission to Moodle.
- To submit to Kaggle, you need to create a specific submission file, which contains the predictions you obtain on the test set. Computing an aggregated evaluation criterion is done automatically by Kaggle
- The format of your submission is rather simple - it is a comma-separated file, where the first column is the identifier of the item that you are predicting, and the second column is the class you are predicting for that item. The first line should include a header, and is should use the names provided in the training set. An example is below:

ID,class  
911366,B  
852781,B  
89524,B  
857438,B  
905686,B  

- There is a limit of 10 submissions per day; finally, you also need to select your top 10 submissions to be counted in the competition
- Before you submit, you should evaluate the classifiers "locally" on your training set, i.e. by splitting that again in a training & test set (or using cross validation), to select a number of fitting algorithms & parameters. Then re-train your best models on the full local training set, and generate the predictions for the test set.
- Evaluation in Kaggle is split in two types of leaderboards - the private and public one. Here, the data is split into 50% / 50%, and as soon as you upload, you will know your results on one of these splits.
The final results will only be visible once the competition closes, and as it is computed on a different split, might be slightly different than what you see initially (e.g. this is similar to a training/test/validation split)
- As it is a competition, there will be bonus points for the top 3 submissions.
- As reproducible science is great, there will be additional bonus points for submissions that use a notebook within the Kaggle competition (note: this was / partially still is called a "kernel" inside the Kaggle competition; Kernel obviously was a confusing term here, as it basically refers to code being executed in the environment of Kaggle itself (e.g. a jupyter notebook, or also a python or R script), and they seem to have realized that, and renamed it). see https://www.kaggle.com/notebooks or https://www.kaggle.com/getting-started/44939. You can first work locally, and then port your code to the notebook version. In Kaggle, your notebook will initially be private. Please share it with me (rmayer, mayer@ifs.tuwien.ac.at), at least, though. You can also make it public at the end of the competition, to show off :-)
We will use the following datasets:

- A small dataset, a good entry point for your experiments

- A larger dataset 

If you want to work as a team, also work on this third dataset:



The Kaggle competition will close on the day displayed in Kaggle. After that, you still have time to submit to Moodle. Your submission to Moodle shall contain:

- A report, containing
  - A description of the datasets, including a short analysis of the features.
  - Details on the software you used for creating your solution
  - The algorithms and parameters you tried
  - The results you obtained on the locally split training/test set
    - And a comparison to the results that you received on Kaggle - how large was the difference, did the rank of the classifiers change (i.e. the first on your training set, was it still the best on the test set on Kaggle?)
-  All the code needed to obtain your results 
- The solution files that you uploaded to Kaggle

You are only allowed to use the training data made available on Kaggle, but no other information!