# Optimal-Influencer-Marketing-Campaign
This repository contains the code related to the papers

- R. Lopez Dawn, A. Giovanidis - Optimal Influencer Marketing Campaign under Budget Constraints using Frank-Wolfe.

One can find here one Python notebook and three folders. Each folder contains the generated datasets and images for each analysis done in the python notebook.

Notebook 'Optimal Influencer Marketing Campaign under Budget Constraints using Frank-Wolfe [GitHub]': In this notebook we evaluate the performance of our models introduced in our manuscript. First, we introduce synthetic networks to analyze the impact of graph structure on the campaign. We discuss and compare our low-complexity fast algorithm and the rule of thumb against alternative algorithms from the literature to analyze their comparative advantage for the specific budgeted portfolio optimization problem. Furthermore, we argue how Nano-, Micro-, and Macro-influencers differ in each of the various graph structure across different algorithms. We numerically investigate the impact of each type of influencers on the different types of networks. Subsequently, we use a real large Twitter database to evaluate the performance of our low-complexity fast algorithm based on Frank-Wolfe, for various campaign objectives. Finally, we perform a sensitivity analysis of the multi-platform model introduced to analyze the potential ROI-ratio resulting from an optimal budget allocation between  networks, one synthetic and the real Twitter data trace. To carry out our evaluations, in such analysis we implement a sparse version of the social influencer selection by the push method for the particular case of α-fairness utility functions.

1. 'Datasets section 5.1' - This folder contains the saved plot of our analysis done in synthetic networks resulting from the python notebook and:

i). Two text files ('Log utility function[AB graph-Optimums and runtimes]' and 'Log utility function[ER graph-Optimums and runtimes]') for the Albert-Barabasi model and the Erdos-Renyi model, which represent the different metrics obtained by maximizing our synthetic networks for the different algorithms and that contain vectors of the form: _[Number of users, Number of edges, Budget, Optimum of FW algorithm, Time of FW algorithm in seconds, Optimum of the PSG method, Time of the PSG method in seconds, Optimum of the Mirror method, Time of the Mirror method in seconds, Optimum heuristic algorithm, Time of heuristic in seconds, Optimum of BIM CELF. Time of BIM CELF]._

ii). Two text files ('Log utility function[AB graph-Influencers]' and 'Log utility function[ER graph-Influencers]') for the Albert-Barabasi model and the Erdos-Renyi model which represents the different distribution of influencers obtained by maximizing our synthetic networks for the different algorithms and that contain vectors of the form: _[Number of users, Number of edges, Budget, Number of Nano-influencers [FW], Number of Micro-influencers [FW], Number of Macro-influencers [FW], Number of Nano-influencers [BIM], Number of Micro-influencers [BIM], Number of Macro-influencers [BIM], Number of Nano-influencers [H], Number of Micro-influencers [H], Number of Macro-influencers [H]]._

2. 'Datasets section 5.2' - This folder contains the saved plot of our analysis done in the Twitter database from the python notebook and:

i). 'Linear utility function':  A text file which represents the different metrics obtained maximizing a linear utility function with δ=10 as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0,]._ 

ii). 'Log utility function':  A text file which represents the different metrics obtained maximizing a proportional fairness criterion with δ=10 as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0]._ 

iii). 'Max min utility function': A text file which represents the different metrics obtained maximizing a max min fairness criterion with δ=10 as campaign objective and that containing vectors of the form: _[Budget, Impressions, Logarithmic utility function, Max-min utility function, Number of influencers, Number of Macro-influencers, Number of Micro-influencers, Number of Nano-influencers, Reach of campaing ε=0]._ 

3. 'Datasets section 5.3' - This folder contains the saved plot of our analysis done in the multi-platform evaluation from the python notebook and:

i). 'Multi-platform evaluation -Artificial and real networks': A text file which represents the relationship between the cost ratio and the ROI ratio from our analysis done on two databases, the Russian databse one simulated network by an Albert-Barabasi model. The text file has the form: _[Cost quotient, ROI quotient, Total ROI, ROI of the Russian databse, ROI of the simulated network]._

We have used in 2. and 3. as input traces from:

Twitter: freely available https://www.kaggle.com/borisch/russian-election-2018-twitter This trace comes from the Russian elections. It contains 181K active users, with 674K original Tweets and 1,27M Retweets.

Some preprocessing - not included here - is necessary to bring the traces to the appropriate input form (per line):

_[TweetID, Timestamp, UserID, RetweetID]._
