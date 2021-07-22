# Revue de littérature - ASS - 22/07/2021

## Jurasfky

- Detecting Stances in Media on Global Warming :

  https://www.researchgate.net/publication/344970996_DeSMOG_Detecting_Stance_in_Media_On_Global_Warming  

  **Abstract** : 

  ```Citing opinions is a powerful yet understudied strategy in argumentation. For example, an environmental activist might say, “Leading scientists agree that global warming is a serious concern,” framing a clause which afﬁrms their own stance (that global warming is serious) as an opinion endorsed ([scientists] agree) by a reputable source (leading). In contrast, a global warming denier might frame the same clause as the opinion of an untrustworthy source with a predicate connoting doubt: “Mistaken scientists claim [...].” Our work studies opinion-framing in the global warming (GW) debate,  increasingly partisan issue that has received little attention in NLP. We introduce DeSMOG, a dataset of stance-labeled GW sentences, and train a BERT classiﬁer to study novel aspects of argumentation in how different sides of a debate represent their own and each other’s opinions. From 56K news articles, we ﬁnd that similar linguistic devices for self afﬁrming and opponent-doubting discourse are used across GW-accepting and skeptic media, though GW-skeptical media shows more opponent-doubt. We also ﬁnd that authors often characterize sources as hypocritical, by ascribing opinions expressing the author’s own view to source entities known to publicly endorse the opposing view. We release our stance dataset, model, and lexicons of framing devices for future work on opinion framing and the automatic detection of GWstance.```

  **Pourquoi c'est intéressant** : Analyse des médias, comme nous. Utilisent BERT. Etude d'une stratégie d'argumentation.

  **Méthodo** : 

  	1. Extraire les "stances" via des règles sur les arbres de parsing sémantique des phrases.   (+ : facile, - : structure anglophone permet de faire ça, impossible de faire ça en français (Rubing a essayé de transférer l'implémentation au français sur demande de Jean-Philippe : ça ne marche que très mal) )
  	2. Classifier avec BERT les stances en agrees/disagrees/neutral pour "Climate change/global warming is a serious concern"

  **Dataset** : Médias assez mixés : 

  <img src="./Capture d’écran 2021-07-22 à 12.00.10.png" alt="Capture d’écran 2021-07-22 à 12.00.10" style="zoom: 50%;" />

  Dataset d'entrainement pour la classif : 2K sentences -> approximativement ce que l'on fait 

  Labels : agrees/neutral/disagrees with "Climate change/global warming is a serious concern"  .

  Annotateurs : AMT, "Following 4 pilot studies, we decided to collect 8 judgements per item (to enable robust analysis of demographic variation in annotator judgements), for a total of 16,400 annotations, paying the California minimum wage of $ 12USD per hour. Using typical exclusion criteria, we recruited a set of 398 qualiﬁed annotators over 5 rounds and had them rate 30-50 items. We also asked for basic demographic information and their personal opinions on a series of questions related to GW (see Appendix D for details and an example)" 

  Inférence : sur 500K stances

  **Performances** : 

  <img src="./Capture d’écran 2021-07-22 à 12.06.11.png" alt="Capture d’écran 2021-07-22 à 12.06.11" style="zoom:50%;" />

  Puis analyse des stratégies linguistiques des gens qui agree/disagree

  