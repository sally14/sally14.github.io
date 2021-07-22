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

  <img src="https://raw.githubusercontent.com/sally14/sally14.github.io/master/data/litt_review/Capture%20d%E2%80%99%C3%A9cran%202021-07-22%20%C3%A0%2012.00.10.png" alt="Capture d’écran 2021-07-22 à 12.00.10" style="zoom: 50%;" />

  Dataset d'entrainement pour la classif : 2K sentences -> approximativement ce que l'on fait 

  Labels : agrees/neutral/disagrees with "Climate change/global warming is a serious concern"  .

  Annotateurs : AMT, "Following 4 pilot studies, we decided to collect 8 judgements per item (to enable robust analysis of demographic variation in annotator judgements), for a total of 16,400 annotations, paying the California minimum wage of $ 12USD per hour. Using typical exclusion criteria, we recruited a set of 398 qualiﬁed annotators over 5 rounds and had them rate 30-50 items. We also asked for basic demographic information and their personal opinions on a series of questions related to GW (see Appendix D for details and an example)" 

  Inférence : sur 500K stances

  **Performances** : 

  <img src="https://raw.githubusercontent.com/sally14/sally14.github.io/master/data/litt_review/Capture%20d%E2%80%99%C3%A9cran%202021-07-22%20%C3%A0%2012.06.11.png" alt="Capture d’écran 2021-07-22 à 12.06.11" style="zoom:50%;" />

  Puis analyse des stratégies linguistiques des gens qui agree/disagree

  

  ## Laura Nelson

  

  

  ## Theocharis & Jungerr 2020

  - Yannis Theocharis & Andreas Jungherr (2020): Computational Social Science and the Study of Political Communication, Political Communication, DOI: 10.1080/10584609.2020.1833121
  - 

  ![Capture d’écran 2021-07-22 à 16.49.15](https://raw.githubusercontent.com/sally14/sally14.github.io/master/data/litt_review/Capture%20d%E2%80%99%C3%A9cran%202021-07-22%20%C3%A0%2016.49.15.png)

  -> Barbera 2020 revient tout le temps



## À partir des citations de Barbera 2021

### Modeling Framing in Immigration Discourse on Social Media  

- Julia Mendelsohn et al., 13 april 2021,  http://arxiv.org/abs/2104.06443

- <img src="https://raw.githubusercontent.com/sally14/sally14.github.io/master/data/litt_review/Capture%20d%E2%80%99%C3%A9cran%202021-07-22%20%C3%A0%2018.04.39.png" alt="Capture d’écran 2021-07-22 à 18.04.39" style="zoom:50%;" />
- "By creating a new dataset of immigration- related tweets labeled for multiple framing typologies from political communication theory, we develop supervised models to detect frames"
- Tweets are annotated using three frame typologies: (i) issue-generic policy, (ii) immigration-specific, and (iii) narrative frames, where a tweet may use multiple frames simulta- neously. We
- Training, development, and test data were annotated using two procedures after four annotators completed four rounds of training. The dataset contains equal numbers of tweets from the EU, UK, and US. Training data was singly annotated and includes 3,600 tweets, while the development and test sets each contain 450 tweets (10% of the full dataset) and were consensus-coded by pairs of trained annotators. 
- <img src="https://raw.githubusercontent.com/sally14/sally14.github.io/master/data/litt_review/Capture%20d%E2%80%99%C3%A9cran%202021-07-22%20%C3%A0%2018.12.44.png" alt="Capture d’écran 2021-07-22 à 18.12.44" style="zoom:50%;" />
- **Experimental Setup** We detect frames for all 2.6M immigration-related tweets using the fine- tuned RoBERTa model with the best-performing seed on development data. Using this labeled data, we estimate the effects of region and ideology by fitting separate mixed-effects logistic regression models to predict the presence or absence of each frame. 
- **Intérêt pour nous** : Très proche de ce que l'on fait en terme de méthodo : mêmes modèles etc. Type de données différent : tweet.

### Framing and Agenda-setting in Russian News: a Computational Analysis of Intricate Political Strategies



- --> Globalement, méthodes basées sur de la lexico



### Super-unsupervised text classification for labeling online political hate

https://www.researchgate.net/publication/352235231_Super-unsupervised_text_classification_for_labeling_online_political_hate



June 2021

- **Abstract** :   We live in a world of text but the sheer magnitude ofsocial media data coupled with a need to measure complex psychological constructs have made this important source ofdata difficult to use for many social scientists. Either researchers engage in costly hand-coding ofthousands oftexts using supervised techniques or in unsupervised techniques where the measurement ofpredefined constructs are difficult. We propose a novel approach which we call super-unsupervised learning using the psychologically complex construct online political hate. This approach draws on the best features from both supervised and unsupervised learning techniques: Measurements of complex psychological constructs without a single labelled data source. We first outline the approach and then provide tests of (i) face validity, (ii) convergent and discriminant validity, (iii) criterion validity, (iv) external validity and (v) ecological validity.

- **Methode** : The "super-unsupervised" technique oﬀers a simple yet elegant solution to the problems of both

  deﬁnition and measurement. The approach makes use of so-called "word embeddings" to identify

  what social media users themselves ﬁnd politically hateful and uses these to construct a classiﬁer for

  the entire corpus. Speciﬁcally, the “super-unsupervised” technique involves a series of simple but

  eﬀective steps: (i) train word vectors for the desired corpus; (ii) use the trained word vectors to extract

  the constructs you are interested in (here, “political hate”); (iii) for each document in the corpus (here,

  social media posts), calculate the distance to the investigated construct; (iv) sort by the calculated

  distance; and (v) appreciate the ﬁnal "labeled” dataset.

- --> Globalement le texte laisse une impression un peu étrange, ça a l'air de mal tenir debout et d'être justifié par des arguments un peu bofs

### Social Media and Political Agenda Setting 

https://doi.org/10.1080/10584609.2021.1910390

- **Abstract** : What is the role of social media in political agenda setting? Digital platforms have reduced the gatekeeping power of traditional media and, potentially, they have increased the capacity of various kinds of actors to shape the agenda. We study this question in the Swiss context by examining the connections between three agendas: the traditional media agenda, the social media agenda of parties, and the social media agenda of politicians. Specifically, we validate and apply **supervised machine learning classifiers** to categorize **2.78 million arti- cles published in 84 newspapers, 6,500 tweets posted on official party accounts, and 210,000 tweets posted by politicians on their own accounts from January 2018 until December 2019**. We first use the classifier to measure the salience of the four most relevant issues of the period: the environment, Europe, gender equality, and immigration. Then, using a vector autoregression (VAR) approach, we analyze the relationship between the three agendas. Results show that not only do the traditional media agenda, the social media agenda of parties, and the social media agenda of politicians influence one another but, overall, no agenda leads the others more than it is led by them. There is one important exception: for the environment issue, the social media agenda of parties is more predictive of the traditional media agenda than vice-versa. These findings underscore how closely differ- ent agendas are tied together, but also show that advocacy campaigns may play an important role in both constraining and enabling parties to push their specific agendas.

- **Methode** : The classifiers are built around an ensemble procedure which uses different algorithms to
  classify the texts (Géron, 2019). The feature engineering is based on a Word to Vector (Word2Vec) approach. Word2Vec is a neural network trained to reconstruct linguistic context of words using a vector space built form a large corpus of words. We base the vector space on our text corpus which enables us to reconstruct the linguistic context of words within the political domain. The ensemble classifiers for tweets and longer texts both perform reasonably well over all topics of interest. The main difference between the two classifier systems, besides the different training data, is that the social media classifier classifies texts into ten different topics, while the second classifier considers a slightly wider range of topics (see also Table A1). The ensemble method results in out-of-sample accuracy of at least 80% for all classes in German and French. Tables A2 and A39 provide detailed information on the classifier performance and underscore that the ensemble methods do not suffer from systematic classification error. The classifier for social media texts has an overall F1 score of 88% in German and 65% in
  French, while the overall classification of newspaper articles has an F1 score of 78% in German and 86% in French. Due to the large amount of training data, we do not need to consider active learning approaches and do not face the issue of imbalanced classes (Fong & Tyler, 2020). Our extensive validation in the Supporting Information underscores that we do not face the issue of systematic misclassification.

