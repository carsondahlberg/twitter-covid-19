# twitter-covid-19
covid-19 twitter research

* carson dahlberg, 2020-04-05
* UCSD Data Science Project

## ideation
* use a curated dataset provided for scientific research reasons
* high-level analysis of the corpus
  * n-gram analysis (1,2,3) over time from provided top 1000 of each
  * language, country, region
* keywords and releated word analysis (twitter targeting):
  * language
  * gender
  * interest
  * follower
  * behavior
  * geography
* corpus word frequencies
* vocabulary of each set and word drift
* sentiment (use a previous classifier from amazon, yelp and apple), or from kaggle toxicity detection website
* keyword analysis (timeseries and counts, topics)
  * initial caronavirus-related keywords: *__coronavirus, 2019nCoV__*
  * collecting tweets specifically using the following data driven selection of keywords: *__COVD19, CoronavirusPandemic, COVID-19, 2019nCoV, CoronaOutbreak,coronavirus , WuhanVirus, covid19, coronaviruspandemic, covid-19, 2019ncov, coronaoutbreak, wuhanvirus__*
  * linked words to the top n-grams


## data [A Twitter Dataset of 100+ million tweets related to COVID-19](https://zenodo.org/record/3735274#.XopzzojYpPY)
* Banda, Juan M., Tekumalla, Ramya, Wang, Guanyu, Yu, Jingyuan, Liu, Tuo, Ding, Yuning, & Chowell, Gerardo. (2020). A Twitter Dataset of 100+ million tweets related to COVID-19 (Version 3.0) [Data set]. Zenodo. http://doi.org/10.5281/zenodo.3735274
* This dataset is released only for research purposes under a [CC0 1.0 Universal (CC0 1.0) Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/)
* [Covid-19 Twitter chatter dataset for scientific use](http://www.panacealab.org/covid19/)
* [https://github.com/thepanacealab/covid19_twitter](https://github.com/thepanacealab/covid19_twitter)
> Due to the relevance of the COVID-19 global pandemic, we are releasing our dataset of tweets acquired from the Twitter Stream related to COVID-19 chatter. The first 9 weeks of data (from January 1st, 2020 to March 11th, 2020) contain very low tweet counts as we filtered other data we were collecting for other research purposes, however, one can see the dramatic increase as the awareness for the virus spread. Dedicated data gathering started from March 11th to March 30th which yielded over 4 million tweets a day. We have added additional data provided by our new collaborators from January 27th to February 27th, to provide extra longitudinal coverage.
The data collected from the stream captures all languages, but the higher prevalence are:  `English`, `Spanish`, and `French`. We release all tweets and retweets on the `full_dataset.tsv` file (101,400,452 unique tweets), and a cleaned version with no retweets on the `full_dataset-clean.tsv` file (20,244,746 unique tweets). There are several practical reasons for us to leave the retweets, tracing important tweets and their dissemination is one of them. For NLP tasks we provide the top 1000 frequent terms in `frequent_terms.csv`, the top 1000 bigrams in `frequent_bigrams.csv`, and the top 1000 trigrams in `frequent_trigrams.csv`. Some general statistics per day are included for both datasets in the `statistics-full_dataset.tsv` and `statistics-full_dataset-clean.tsv` files. 

## data description
As part of our normal daily data collection from the publicly available Twitter stream, we get around 4.4 million tweets a day. From that collection we started analyzing the uptick on Coronavirus related keywords (coronavirus , 2019nCoV) when we first searched for them on February 11th. The tweets we found (the identifiers that is) are available from January 1st to March 11th, this later date is when we started collecting tweets specifically using the following data driven selection of keywords: COVD19, CoronavirusPandemic, COVID-19, 2019nCoV, CoronaOutbreak,coronavirus , WuhanVirus, covid19, coronaviruspandemic, covid-19, 2019ncov, coronaoutbreak, wuhanvirus. These keywords have been used to exclusively grab tweets from the stream API since then, yielding around 4.4 million tweets a day and the bulk of the data found in this dataset.

## resources
* [Machine Learning in Python: Main Developments and Technology Trends in Data Science, Machine Learning, and Artificial Intelligence](https://www.mdpi.com/2078-2489/11/4/193)
* workshops
  * https://aiforsocialgood.github.io/neurips2019/
  * https://aiforsocialgood.github.io/iclr2019/
  * https://spssi.onlinelibrary.wiley.com/journal/15404560
* [Data Science for Good](https://medium.com/lingvo-masino/nlp-for-social-good-part-i-85b2d757bf15)
  * Ji, S., Pan, S., Li, X., Cambria, E., Long, G. and Huang, Z., 2019. Suicidal Ideation Detection: A Review of Machine Learning Methods and Applications. arXiv preprint arXiv:1910.12611.
  * Pennell, D.L. and Liu, Y., 2014. Normalization of informal text. Computer Speech & Language, 28(1), pp.256–277.
  * Satapathy, R., Guerreiro, C., Chaturvedi, I. and Cambria, E., 2017, November. Phonetic-based microtext normalization for twitter sentiment analysis. In 2017 IEEE International Conference on Data Mining Workshops (ICDMW) (pp. 407–413). IEEE.
  * Y.-P. Huang, T. Goh, and C. L. Liew, “Hunting suicide notes in web 2.0-preliminary findings,” in Multimedia Workshops, 2007. ISMW’07. Ninth IEEE International Symposium on. IEEE, 2007, pp. 517–521.
  * A. Shepherd, C. Sanders, M. Doyle, and J. Shaw, “Using social media for support and feedback by mental health service users: thematic analysis of a twitter conversation,” BMC psychiatry, vol. 15, no. 1, p. 29, 2015.
  * M. De Choudhury and S. De, “Mental health discourse on reddit: Self-disclosure, social support, and anonymity.” in ICWSM, 2014.
  * [14] X. Huang, L. Zhang, D. Chiu, T. Liu, X. Li, and T. Zhu, “Detecting suicidal ideation in chinese microblogs with psychological lexicons,” in Ubiquitous Intelligence and Computing, 2014 IEEE 11th Intl Conf on and IEEE 11th Intl Conf on and Autonomic and Trusted Computing, and IEEE 14th Intl Conf on Scalable Computing and Communications and Its Associated Workshops (UTC-ATC-ScalCom). IEEE, 2014, pp. 844–849.
  * [15] X. Huang, X. Li, T. Liu, D. Chiu, T. Zhu, and L. Zhang, “Topic model for identifying suicidal ideation in chinese microblog,” in Proceedings of the 29th Pacific Asia Conference on Language, Information and Computation, 2015, pp. 553–562
  * M. J. Vioules, B. Moulahi, J. Aze, and S. Bringay, “Detection of suicide-related posts in twitter data streams,” IBM Journal of Research and Development, vol. 62, no. 1, pp. 7:1–7:12, 2018.
  * F. Ren, X. Kang, and C. Quan, “Examining accumulated emotional traits in suicide blogs with an emotion topic model,” IEEE journal of biomedical and health informatics, vol. 20, no. 5, pp. 1384–1396, 2016.
* [AI for Social Good ICML2019 Workshop](https://aiforsocialgood.github.io/icml2019/)
* [Martens, Daniel and Maalej, Walid, "Extracting and Analyzing Context Information in User-Support Conversations on Twitter", 31 July, 2019, arXiv:1907.13395v1](https://arxiv.org/pdf/1907.13395.pdf)
* [Opinion Mining, Sentiment Analysis, and Opinion Spam Detection, Bing Liu. Sentiment Analysis and Opinion Mining, Morgan &
Claypool Publishers, May 2012](https://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html)
  * opinion lexicon
  * comparative words
  * [Sentiment Analysis and Opinion Mining](https://www.cs.uic.edu/~liub/FBS/SentimentAnalysis-and-OpinionMining.pdf)
* [py ds ref code](https://www.earthdatascience.org/courses/use-data-open-source-python/intro-to-apis/calculate-tweet-word-frequencies-in-python/)
  * remove urls, text cleanup, stopwords, vocabs, etc
* [Sentiment with NLTK](http://www.laurentluce.com/posts/twitter-sentiment-analysis-using-python-and-nltk/)
* [Sentiment Considerations](http://help.sentiment140.com/for-students/)
* [Twitter Sentiment Classification using Distant Supervision](https://cs.stanford.edu/people/alecmgo/papers/TwitterDistantSupervision09.pdf)