# Optimal-Influencer-Marketing-Campaign
This repository contains the code related to the papers

- R. Lopez Dawn, A. Giovanidis - Optimal Influencer Marketing Campaign under Budget Constraints using Frank-Wolfe.

One can find here one Python notebook and three folders. Each folder contains the generated datasets and images for each analysis done in the python notebook.

Notebook "Optimal Influencer Marketing Campaign under Budget Constraints using Frank-Wolfe [GitHub]": In this notebook we evaluate the performance of our models introduced in our manuscript. First, we introduce synthetic networks to analyze the impact of graph structure on the campaign. We discuss and compare our low-complexity fast algorithm and the rule of thumb against alternative algorithms from the literature to analyze their comparative advantage for the specific budgeted portfolio optimization problem. Furthermore, we argue how Nano-, Micro-, and Macro-influencers differ in each of the various graph structure across different algorithms. We numerically investigate the impact of each type of influencers on the different types of networks. Subsequently, we use a real large Twitter database to evaluate the performance of our low-complexity fast algorithm based on Frank-Wolfe, for various campaign objectives. Finally, we perform a sensitivity analysis of the multi-platform model introduced to analyze the potential ROI-ratio resulting from an optimal budget allocation between  networks, one synthetic and the real Twitter data trace. To carry out our evaluations, in such analysis we implement a sparse version of the social influencer selection by the push method for the particular case of α-fairness utility functions.


1. "Participation ratios_Linear function": A text file containing vectors of the form: _[Budget, UserID, Participation ratio]_ which represents that the user with  _UserID_ joins in the campaign of _Budget_ [EUR/day] with a _Participation ratio_ in order to maximize our campaign following a linear function.

2. "Participation ratios_Log utility function": A text file containing vectors of the form: _[Budget, UserID, Participation ratio]_ which represents that the user with  _UserID_ joins in the campaign of _Budget_ [EUR/day] with a _Participation ratio_ in order to maximize our campaign following a proportional fairness criterion (logarithmic function).

3. "Participation ratios_Max min utility function": A text file containing vectors of the form: _[Budget, UserID, Participation ratio]_ which represents that the user with  _UserID_ joins in the campaign of _Budget_ [EUR/day] with a _Participation ratio_  in order to maximize our campaign following a max min fairness criterion (max min function).

4. "Linear utility function":  A text file which represents the different metrics obtained maximizing a linear utility function as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0, Reach of campaing ε=δ]._ 

5. "Log utility function":  A text file which represents the different metrics obtained maximizing a proportional fairness criterion as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0, Reach of campaing ε=δ]._ 


6. "Max min utility function": A text file which represents the different metrics obtained maximizing a max min fairness criterion as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0, Reach of campaing ε=δ]._ 

7. "Sub-linear convergence": A text file of the form: _[Number of iteration, Marginal growth of the objective function at each step]_ that replicates an example of our sub-linear convergence rate with a stopping criterion when the number of iterations reaches a maximum equal to 30, or when the infinite norm of solutions between iterations is less than 0.1\%.

We have used as input for the above programs, traces from:

Twitter: freely available https://www.kaggle.com/borisch/russian-election-2018-twitter This trace comes from the Russian elections. It contains 181K active users, with 674K original Tweets and 1,27M Retweets.

Some preprocessing - not included here - is necessary to bring the traces to the appropriate input form (per line):

_[TweetID, Timestamp, UserID, RetweetID]_
