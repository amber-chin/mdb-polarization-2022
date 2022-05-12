# mdb-polarization-2022

This is the repository for the paper **"Evaluating Digital Polarization in Multi-Party Systems: Evidence from the German Bundestag"** by Amber Chin, Carolina Coimbra Vieira, and Jisu Kim (2022).

## Project Overview
We use Twitter data for the year 2020 to identify polarization trends among members of the German Bundestag. Specifically, we evaluate trends on the levels of retweets, mentions, and following-follower relationships. We do this by **(1)** performing a network analysis for each network level and **(2)** performing a sentiment analysis of the Twitter mentions between Bundestag members.

## Data files
The data available in this repo track Bundestag member Twitter interactions for 2020. For the retweets and mentions networks, edge weights are determined by the number of repeat interactions that occur between a given pair of Bundestag members. 

**Node tables**
- node_retweets.csv
- node_mentions.csv
- node_following-follower.csv

**Edge tables**
- edge_retweets.csv
- edge_mentions.csv
- edge_following-follower.csv


## Results
Network statistics for each level of analysis can be found in the table below. Network visuals were created in Gephi such that each party is represented by a different color: *red* = SPD, *green* = Die Grünen, *yellow* = FDP, *blue* = AfD, *gray* = CDU/CSU, and *pink* = Die Linke. Node size is determined by the number of in-degree connections each member has (**NOTE**: the networks include instances of self-retweeting or self-mentioning).

| **Metrics**          | **Retweets** | **Mentions** | **Following-follower** |
|------------------|----------|----------|--------------------|
| # nodes          | 470      | 394      | 553                |
| # edges          | 7376     | 2084     | 44555              |
| Avg. degree      | 15.694   | 5.289    | 80.57              |
| Diameter         | 6        | 8        | 5                  |
| Modularity       | 0.807    | 0.416    | 0.430              |
| # communities    | 6        | 7        | 5                  |
| Density          | 0.033    | 0.013    | 0.146              |
| Avg. path length | 3.117    | 3.52     | 2.007              |


**Retweets network**

<img src="https://user-images.githubusercontent.com/55859245/168030540-14b249b2-c552-4184-b509-a73c8e4fce9e.png" width="60%">

**Mentions network**

<img src="https://user-images.githubusercontent.com/55859245/168032972-d075c0a6-b31b-434f-bfa1-640b132f5667.png" width="60%">


**Following-follower network**

<img src="https://user-images.githubusercontent.com/55859245/168033077-85a7bdb2-ba6b-4d57-a253-f258b3d6c179.png" width="60%">


**External-Internal Index**

To evaluate polarization levels, we calculate an External-Internal (E-I) Index for each network (Krackhardt and Stern 1988). This is done by calculating the number of *inter-* party interactions relative to the *intra-* party interactions. The E-I index is a value between [-1,1] that indicates the level of homophily for a given group, which in our case refers to a political party, such that a value of -1 means all connections are internal to the group and a value of +1 means all connections are external to the group. 

<img width="400" alt="ei_index_plot" src="https://user-images.githubusercontent.com/55859245/168038571-9feb9230-b494-46d4-91b1-ce987bfaed66.png">

**Sentiment analysis of the mentions network**

We use tweets in German that contain a mention of a single Bundestag member for the sentiment analysis (*N* = 3,


## Reference Paper
For further information, see: 

> Amber Chin, Carolina Coimbra Vieira, and Jisu Kim. 2022. Evaluating Digital
Polarization in Multi-Party Systems: Evidence from the German Bundestag.
In 14th ACM Web Science Conference 2022 (WebSci ’22), June 26–29, 2022,
Barcelona, Spain. ACM, New York, NY, USA, 6 pages. https://doi.org/10.1145/3501247.3531547
