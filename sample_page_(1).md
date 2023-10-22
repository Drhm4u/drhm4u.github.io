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

For more details, you can check out [my Kaggle Notebook](https://www.kaggle.com/code/stphanedrihem/will-they-open-a-term-deposit/).
