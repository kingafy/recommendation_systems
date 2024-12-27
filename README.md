# recommendation_systems
https://github.com/robi56/Deep-Learning-for-Recommendation-Systems

https://github.com/AlessandroCorradini/University-of-Minnesota-Recommender-System-Specialization

https://github.com/LaxmiChaudhary/Amzon-Product-Recommendation/blob/master/Recommendation%20System.ipynbhttps://github.com/caserec/Datasets-for-Recommender-Systems

https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html

Recommender data sets :-->https://github.com/caserec/Datasets-for-Recommender-Systems
Few more datasets
https://cseweb.ucsd.edu/~jmcauley/datasets.html



https://github.com/rahul-dhavalikar/Product-Recommendation-System/blob/master/product-recommendation-system.ipynb  amazon based

https://github.com/nihal223/Amazon-Product-Recommendation-System/blob/master/Recommender%20Implement.ipynb

Apparel based https://github.com/GuptaAB/Apparel-Product-Recommendation-Engine/blob/master/RecommenderEngine.ipynb

Spark-defaults.cof template ;;--uncomment the spark driver memory

Amazon uses collaborative

Research work:--https://github.com/robi56/Deep-Learning-for-Recommendation-Systems

Types of Recommendation Systems
Content Based
Collaborative(scalability issue at times(items based is simpler)apache is batter fit to make scalable. Noisy to sparse data
Graphical
Knn recommenders
Hybrid
Model based like SVD/SVD++
Deep learning based/RBM
Attention based
RL based
Translation based  (ruinin-he)(seq based product search)
SLIM method

Amazon DSSTNE (distributed based sparse based NN==used for recommender












https://paperswithcode.com/sota/collaborative-filtering-on-movielens-1m
https://paperswithcode.com/task/recommendation-systems/codeless?page=17

https://github.com/LaxmiChaudhary/Amzon-Product-Recommendation/blob/master/Recommendation%20System.ipynb

https://github.com/smwitkowski/Amazon-Recommender-System/blob/master/Collaborative%20Filtering%20Amazon%20Watch%20Reviews.ipynb

https://github.com/rahul-dhavalikar/Product-Recommendation-System/blob/master/product-recommendation-system.ipynb

https://github.com/JackHannnnnn/Amazon-Recommender-System







KNN Recommenders





Knn does not work well
Knn considers it be continous problem instead of classification



Difference between KNN and collaborative
1st approach (KNN/profiles similarity)
First of all, KNN is not the main feature of the first approach. It's just an algorithm to find nearest items among the whole collection, so it can be used in collaborative filtering as well. The most important idea lies in a term "similarity". To recommend something to the user in question, you find people from his neighborhood that have similar profile. For example, you want to make recommendation for user John on the Facebook. You look at his Fb profile and then at profiles of his friends. You find 10 people with similar profiles and check what they like. If 8 of 10 people with similar profiles like new film, most probably John will like it too.
So, there are 2 important points here:
	• you look at user's neighborhood
	• you measure similarity of their profiles
Wikipedia article doesn't cover question of how to find similarity measure, but there are many ways, including searching for common terms in profile's text, finding best friends (my number of messages between them, connection graph analysis, etc.) and many others.
2nd approach (collaborative filtering)
In the second approach you don't need to analyze neighborhood and find similar profiles, but you need to collect users choices. Let's recall an example with Facebook user John. Imagine, that we can get all "likes" of all Fb users, including those of John. With them you can build very large correlation matrix, where rows are user ids and columns are all possible items they may "like". If the actually "liked" an item, cell for current user and current item is set to 1, otherwise it is 0.
With such a matrix (built or abstract) you can use association mining to find the most strong associations. For example, 10000 people who liked "Pirates of the Caribbean 2" also liked "Pirates of the Caribbean 3", but only 500 of them liked "Saw". So we can suppose that association between 2 episodes of "Pirates" is much stronger. Note, that we haven't analyzed neither users, nor films themselves (we didn't take into account film names, plots, actors or something like that - only "likes"). This is major advantage of collaborative filtering over methods based on similarity.
Finally, to recommend film to out user John you just iterate over his "likes" and find other items that have strongest associations with the current one.
So, important points here are:
	• you don't use neighborhood, but instead complete database of all users
	• you use people's choices and find associations
Both approaches have their strong and weak points. 1st approach is based on some kind of connections between people (e.g. friends on Facebook) and hardly can be used for services like Amazon. At the same time 2nd approach is based on the averaged preferences of all users and thus isn't good option for systems with highly different favors.

From <https://stackoverflow.com/questions/7742706/k-nearest-neighbour-vs-user-based-nearest-neighbour> 

http://recommender-systems.org/collaborative-filtering/

https://www.elenacuoco.com/2016/12/22/alternating-least-squares-als-spark-ml/







Complexity surrounding Recommender systems






RBM :-http://www.cs.utoronto.ca/~hinton/absps/netflixICML.pdf




https://www.slideshare.net/gabrielspmoreira/deep-learning-for-recommender-systems-tdc-sp-2019?qid=7d43c434-fe67-4973-b06d-0722a5736fde&v=&b=&from_search=7   good material for RS
Tutorial on Deep Learning in Recommender System, Lars summer school 2019

https://github.com/awarebayes/RecNN

https://github.com/cszhangzhen/DRL4Recsys   papers on RLRS

Papers with code
https://paperswithcode.com/paper/recogym-a-reinforcement-learning-environment#code

Papers for RL in Recsys
https://github.com/cszhangzhen/DRL4Recsys

Good tutoral for starters for DL in Speech
https://missinglink.ai/guides/tensorflow/tensorflow-speech-recognition-two-quick-tutorials/

Deep learning and RL in RS :-https://www.slideshare.net/AnoopDeoras/tutorial-on-deep-learning-in-recommender-system-lars-summer-school-2019?qid=fd7af205-3335-4c32-9dc4-9d3f7c8dc91b&v=&b=&from_search=2

https://paperswithcode.com/search?q_meta=&q=Reinforcement+Learning+based+Recommender





Content based similarity measures:-









You want to create a hybrid recommendation system to suggest music for new users on your music streaming app that just launched. New users are asked to rate a few bands that they like. You have reliable data for artist name, song name, album name, etc., and each song is also labeled for genre but at a somewhat coarse level (rock, pop, etc.). Which component of your recommendation system will likely perform the best?

From <https://www.coursera.org/learn/recommendation-models-gcp/exam/9yE4H/neural-networks-for-recommendations-quiz/attempt?redirectToCover=true> 





![image](https://github.com/user-attachments/assets/7b0156ab-28af-4730-88cc-3a080c25aaf8)
