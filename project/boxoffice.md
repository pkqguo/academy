Box Office Prediction
===

##背景##
------------

Google has published a technical whitepaper in June 2013, revealing the correlation between the successfulness and the number of Google searches of a movie.

**Quantifying Movie Magic Research Studies** [[view]](files/quantifying-movie-magic_research-studies.pdf)

------------

##项目进展##
------------

####本项目目前主要参考的特征包括####
1. 电影名的百度指数在上映前一周之前的总和；
2. 豆瓣的短评数、评论数在上映前一周之前的总和。

####未来计划加入的特征包括####
1. 电影的静态特征，如导演、演员、是否好莱坞大片（发行公司），等；
2. 电影档期的因素，和同档期各电影的竞争因素。

####本项目采用的机器学习模型及策略####
1. 目前采用kNN模型，在所有标注集上使用单一模型；
2. 未来计划分割特征空间，并在每一个子空间上训练不同的子模型，提高预测的准确率。

-----------

##实时预测结果（首周票房）##
* 美国队长2（2014.4.4上映）：2880,3411元
* 三小强（2014.4.4上映）：30,0175元
* 整容日记（2014.4.4上映）：720,5272元
* 笔仙惊魂3（2014.4.4上映）：112,9357元



