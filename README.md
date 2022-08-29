# comp309-a3
COMP 309 Assignment 3: Kaggle Competition

# IF you want the assignment's solution, please add my wechat: fuji12345

1 Objectives

The goal of this assignment is to help you tie together all the concepts you have learnt in the first half of this course

in the lectures and assignments. To aid you in completing this assignment, you should review the major aspects of

the course that have been explored so far, such as:

• Data understanding, cleansing, and pre-processing,

• Machine learning concepts,
• CRISP-DM and pipelines in general,
• Feature manipulation, including feature selection, feature construction and imputation,
• Statistical design and analysis of results.
These topics are (to be) covered in Weeks 1–7. Research into online resources for AI is encouraged, where the
rabbit-hole1 will provide useful jumping off points for further exploration.
2 Question Description

Many of us use some music streaming app to listen to music. These apps usually make personalized playlists to cater
to each user’s need. But what is the logic behind the personalized playlist? One general example is to have a Music
Genre Classification System. More specifically, creating a machine learning model, which classifies music samples
into different genres using various audio features.
The overall aim of this assignment is to develop the best possible machine learning system to predict the genres of
music. The task is to classify the music tracks into one of ten genres based on the provided audio features. The
data for each track includes both textual features e.g. artist and track names, numerical descriptors e.g. duration
and various audio features. The hope is that your model will identify the relationship between music genres and the
audio features.
We have set up a Kaggle InClass Competition2
to facilitate finding the best machine learning system for officials to
use. You are expected to analyse the provided data, design and improve your own machine learning pipeline, and
consider the consequences of applying your pipeline to this data.
Note the data is real. Thus, you could attempt to find the original dataset and create a look-up table. This is not
permitted as it misses the point of the course. We want to see your analyses, rather than see perfect results.

2.1 Preliminary: Accessing the Kaggle InClass Competition
To access the class competition, you must use the below url. Please do not share this publicly as it will allow
anybody to access our competition, which will make the experience less enjoyable for your classmates. Deliberate
cheating is a disciplinary matter, so please don’t go there either.
Competition link: https://www.kaggle.com/t/59de28f43fe94576bb7044d28b3d5965
You will need to register a Kaggle account. It is perfectly fine (and expected) to use a pseudonym as your Kaggle
username so your classmates do not know your real-life identity. However, you will need to fill out the following
form so that the lecturers and tutors can link your Kaggle result to your ECS account. No other people will have
access to this information! Each time you change your Username, please update the form (it would make sense to do
this only once, but past experience suggests that students will change their Username a few times). We cannot give
credit to top-scoring students if we cannot link a username to an actual/course name! Usernames must be suitable
for work and respectful.
Please fill out the following form:
https://forms.office.com/r/EgdbpuNe5E
Please submit as part of your report.
Once you have completed the above steps, please verify that you can access the following page:
https://www.kaggle.com/competitions/comp309-2022/overview (when logged in).
Once successful, please accept the terms of the competition so that you may proceed to the rest of the assignment!
2.2 Core: Exploring and understanding the Data [40 marks]
We have created a processed version of the music genres data. This is to be used in the classification competition.
We have split the data into training and test set.
The training set is to be used to create your model. You can use any machine learning tool, e.g. Orange, Scikit-learn.
Your model will need to be able to predict the class of ‘unseen’ test data (i.e. features, but not class, are provided).
It is often much more effective to first learn about the properties of a dataset (business and data understanding)
before applying machine learning to it. You should begin by familiarising yourself with the dataset by reading the
“Overview” and “Data” tabs of the Kaggle competition. Please download the dataset from the Data tab (in .csv
format). You should now spend some time examining the data and taking notes of any interesting patterns you find.
Requirements
Using any tools you find useful, you should explore and analyse the dataset. You should draw upon your previous
experiences and what you have learnt in this course to find a number of interesting patterns. You may wish to start
by examining the quality, completeness and representation of individual features.
In your report, you should spend no more than 2.5 pages describing the following regarding the Core part:
• (20 marks) Highlight the findings of your dataset exploration. You should identify four important patterns
(e.g. large correlation between variables), and discuss the potential consequence this may have on your results.
To achieve a high mark, you should consider more complicated patterns, such as feature interactions. Use your
judgement and justify what is an important pattern.
• (20 marks) Visualisation is an important aspect of this task. Please illustrate at least one important finding of
your work using visualisation. For full marks, you should be expected to use more than a simple scatter plot.

2.3 Completion: Developing and testing your machine learning system [50 marks]
You may use any ML tools you wish, but a good solution will consider a number of factors, such as: pre-processing
steps, the properties of the dataset and generalisation/over-fitting. Decisions around how to split your labelled data
into training/testing/cross-validation set/s are your choice, which are important and should be explained.
Your file will need to consist of two columns. The “instance_id" and the “genre" only. The csv should include your
predictions for all instances in the dataset, plus a header line (30,932 lines). For example:
instance_id, music_genre
1, Comedy
2, Electronic
3, Hip-Hop
...
30931, Soul
Part of the test data is to be used by Kaggle to test your model in order to create the public leaderboard. The
remaining part of the test set is used by Kaggle to test your model for the private leaderboard. You will submit
your complete answer to the test set but will not know which instances have been used for the public or private
leaderboard (this helps prevent over-fitting and gaming the system).
Once you are satisfied with your initial attempt (do not spend too long on it!), you should upload your output csv to
the submissions page of the competition: https://www.kaggle.com/competitions/comp309-2022/submissions.
Once your submission has been processed, you will be able to see your classification accuracy on the public leaderboard. You should use this feedback to further improve your system. For example, if your leaderboard performance is
much lower than on your own test set, you have over-fitted your model. You should use your judgment to decide how
extensively to change your system. This may only be tweaking parameters, or you may decide to try a completely
different algorithm. Note that you are limited to 5 submissions per day, but submitting this many may be to your
detriment as you may “over-train” on the public leaderboard!
Note that: do not be discouraged if your performance appears low on the leaderboard: we are interested in
novel/interesting solutions even if they have lower performance, and you may come out on top on the private
leaderboard anyway.
Requirements
You should refine your machine learning system a number of times (at least 3, including the initial system) based
on the performance you achieve on the public leaderboard. Your submitted report should contain up to 4 pages
regarding the Completion component:
• (15 marks) Discuss the initial design of your system, i.e. before you have submitted any predictions to the
Kaggle competition. Justify each decision you made in its design, e.g. reference insight you gained in the Core
part.
• (25 marks) Discuss the design of one or more of your intermediary systems. Justify the changes you made to
the previous design based on its performance on the leaderboard, and from any other additional investigation
you performed.
• (10 marks). Use your judgement to choose the best system you have developed — this may not necessarily
be the most accurate system on the leaderboard. Make sure you select this submission as your final
one on the competition page before the deadline. Explain why you chose this system, and note any
particularly novel/interesting parts of it. You should submit screen captures and/or the source and executable
code required to run your chosen submission so that the tutors can verify its authenticity.

2.4 Challenge: Reflecting on your findings [10 marks]
Until now, we have been focusing on achieving the best performance possible — but there should be some other
aspects that ML tool users should consider, e.g. the interpretability of the model.
Requirements
You should consider the interpretability of your final chosen model in this part. Your report (1 page on the Challenge
component) should address the following questions:
• (10 marks) How easy is it to interpret your chosen machine learning model, i.e. how easy to comprehend why
certain predictions have been made?
If your model is difficult to interpret, do you see any problems with this? (e.g. whether users will trust your
model? whether it is difficult for the deployment of your solution or to use the model? and so forth.) How
would it compare to a simpler model, e.g. a simple K-Nearest neighbour?
If your model is easy to interpret, what are its limitations? (e.g. whether it can catch the underlying relationship
in the data? whether it can provide accurate predictions?) How would it compare to a more complex model,
such as a ensemble method (e.g. random forest)?
3 Relevant Data Files and Kaggle Information
The datasets, and additional information about the Kaggle competition can be found online:
https://www.kaggle.com/competitions/comp309-2022/
