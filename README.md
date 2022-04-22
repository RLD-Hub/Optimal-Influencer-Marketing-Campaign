# Optimal-Influencer-Marketing-Campaign
This repository contains the code related to the papers

- R. Lopez Dawn, A. Giovanidis - Social Influencer Selection by Budgeted Portfolio Optimization, WiOpt 2021.

One can find here one Python notebook and seven text files:

Notebook "Social Influencer Selection by Budgeted Portfolio Optimization [GitHub]": the notebook implements a sparse version of the social influencer selection for the α-fairness utility functions. We evaluated the performance of our algorithms for various campaign objectives using information from the 2018 Russian elections database. The program is designed to take as input the Leader Graph and the posting and re-posting activity rates of all the users, that can be estimated by real-world traces. The code can solve for millions of users. 

In particular for the 2018 Russian elections database, we used our code to obtain the social influencer selection for a user with 15 followers which is potentially a Micro-influencer (like many stores that provide services in a certain medium-populated area) for a diverse budget campaigns from one euro per day until 50,000 euros per day. We obtained the following text files:

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
