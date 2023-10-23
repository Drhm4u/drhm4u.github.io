## Who will open a term-deposit ?

**Project description** <br>
The idea of this project is to get insights on :<br>
- who is likely to open a term-deposit (analysing people's situation).<br>
- what behaviour does the bank should adopt in regard of the canvassing done.

<br>*Nota* : We expect a lot from the Exploratory Data Analysis to get those insights

The second goal is to model an algorithm that will classify targeted people whether they open a term-deposit or not. This will help the bank advisor to focus his attention on the most likely positive outcome people. 

Here are the **insights of** what datas highlighted in **our analysis** :

- Terms deposits are more likely to be done by young and old people.
- Life's already organized when married compared to single (less opening when married than when single).
- Being contacted by phone is a better way to conclude a term deposit than another one.
- There's more chances to conclude to a term deposit with the more well paid people than others.
- Personal loans influences the rate of default (Default people are unlikely to open a term-deposit compared to others).
- There is nothing that indicates from housing loan that people will be likely to be in default.
- It's a good thing to contact again customers targeted by the campaign to follow-up and ask for a decision.
  + BUT, before doing that : you better let people think before (analysis shows that a certain time between 2 contact has a better outcome than none).
- The chances for an opening (term-deposit) is even better when the targeted client was contacted before the campaign.
  + In that observation, we can assume that the client has already developed a trustworthy relationship with the bank before the campaign and the client is more aware of the advantages that bank may offer (previously sensitized).
  + *Nota* : You surely can't contact people before campaign when it's the first time you reach out to them. But, it would maybe be a good thing to sensitize them in another way at first sight (in a softer way than wanting them to open a term-deposit). There are prior things to do first with a new potential target. In this process, you may get a better rate of opening a term-deposit but in a longer range of time.

**Modeling**<br>
The best models which offers performing results and reduce the overfitting are the VotingClassifier and the SVM model.<br>
As said in the introduction, making a model to classify the targeted people can help bank advisor to focus his attention to the more likely one. This would eventually shorten the effort and maximize the positive outcome. 

**Cumulative gain**
The dataset is really balanced in the possibles outcome. We get half chance of having a positive or negative answer from the targeted client. We can target around 80% of the positive outcome in 50% of the sample. Same note for the negative outcome :<br> 
<img src="images/cumulative_gain_bank.PNG?raw=true" width="400" height="300"/>

The better methodology is to handle the client who has the best probability of opening a term deposit and so on.

 **Conclusion**
 Several conclusions appear in our business case. <br>
 - Either we proceed to the campaign and have immediate effects on opening term-deposit
 - Or we try to reach potential customer in a softer way (making the bank known, attract client with sponsorship bonus, ...) and get to talk about term deposit months or years after.

We might have better results in the second methodology : 67% of positive outcome when client had already contact with bank before campaign against 59% in the other case. But the second strategy is more time consuming than the first one. 
I guess that **time** will be the criteria that will decide the one or second strategy in regard of the benefit it could give : 
67% - 59% = 8%. Does those 8% worth the try to wait many times more or not ?  

For more details, you can check out [my Kaggle Notebook](https://www.kaggle.com/code/stphanedrihem/will-they-open-a-term-deposit/).
