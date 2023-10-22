## Quelles sont les émissions de CO2 d'une voiture ?  

**Description et but du projet** <br>Ce projet consiste à observer quels sont les facteurs qui expliquent les émissions de CO2 d'une voiture. <br>L’idée sous-jacente est d’identifier les véhicules polluants afin que les décideurs publics puissent mettre en place des actions pour favoriser l'achat de véhicules peu polluants (bonus/malus, etc...). 
<br><br>Dans la partie de modélisation, plusieurs algorithmes sont entraînés dans un but de comparaison. La finalité consiste à départager les algorithmes entre eux (choisir le meilleur algorithme à mettre en place dans l'environnement de production) en pesant la performance, le temps de calcul mais aussi l'interprétabilité. 
<br><FONT size="2pts">*Nota* : Les données sont extraites du site data.gouv.fr sur les véhicules commercialisés en 2012, 2013 et 2014.</FONT>

**Conclusion de la modélisation**<br>
Après toutes les étapes d'EDA, de pre-processing et de feature engineering, nous pouvons présenter ce tableau récapitalatif : <br> 
<img src="images/tableau_modelisation_CO2.PNG" width="400" height="350"/>
<br>
<FONT size="2pts">**rf_200** = Random Forest (200 itérations d'arbres)<br>
**StackingReg1** = Stacking sans l'inclusion de l'arbre de décision (contrairement à StackingReg).<br>
**rf** = Random Forest sans features spécifiques.<br>
**dt** = Arbre de décision sans features spécifiques.<br>
**VotingReg1** = Voting sans l'inclusion de l'arbre de décision (contrairement à VotingReg).<br>
**lr** = Régression linéaire.<br>
**best_svm** = SVM avec les meilleures features trouvées au moyen de GridSearch.<br>
**ada_lr** = Ada Boosting en partant d'une base de régression linéaire.<br>
**ada_dt** = Ada Boosting en partant d'une base d'arbre de décision (modèle par défaut).<br>
**svm_model** = SVM sans features spécifiques.</FONT><br>

Le choix du modèle est assez ouvert car les performances de tous s'équivalent.  

S’il y a plusieurs modèles parmi lesquels choisir (car les performances s’équivalent), deux critères de plus peuvent être pris en considération :
-	Temps de calcul
-	Interprétabilité des modèles<br>

En voici le détail :<br>
<img src="images/Choix_modele_CO2.PNG" width="500" height="125"/>
<br><FONT size="2pt"> *Les modèles ne proposent pas de récupérer l’ordre d’importance des features quant à leur impact sur la sortie du label (contrairement à l’arbre de décision, la régression et le randomforest). Il faudrait utiliser des méthodes plus approfondies pour obtenir les informations d’interprétabilité (via SKATER, LIME ou SHAP).</FONT><br><br>
Selon une analyse succincte, on peut retenir la régression linéaire comme étant la plus adaptée à notre problème. 

### Détail du projet
Pour une présentation exhaustive, vous pouvez retrouver [mon rapport d'étude](https://1drv.ms/b/s!AvHm4Ey0oAB0ikj81fSlREuDg_CO?e=rxVKnr/) et [mon notebook](https://colab.research.google.com/drive/1pqc4teWw9T0bCkp6vWxCOZl9Uv0PmzOX?usp=sharing/). 
