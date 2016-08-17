Using command line to use LeadLDA:

java -Dfile.enconding=utf-8 -jar leadlda.jar var1 var2 var3 var4

where	var1 = message file
		var2 = vocab file
		var3 = # of topics
		var4 = path to output model

In terms of format of message file and vocab file, please refer to the following information about msg-wids.data and weibos.vocab respectively.

The dataset in ./data/ contains messages that can be used for topic extraction from Sina Weibo, a Twitter-like microblog website in China. This data-set contains messages posted from May to July, 2014 and is splitted into three sub-sets. Each contains microblog messages posted in May, June, and July, respectively. 

In each subset, there are four data files.

weibos.vocab: The vocabulary of this subset. Each line covers a word and its word id segmented by \t. 

msg-wids.data: Each line covers a message m including its id, pid, leader probability (predicted by pre-trained CRF based leader detection model), and the word ids appearing in m. Messages in the same tree are grouped together in BFS order

msg-hashtag.data: Each line covers a message m including its id and hashtag id. 

hashtags.map: Each line is a pair of hashtag id and the name of the hashtag, given by its author as topic annotation.

If you would like to use LeadLDA or the dataset for your research works, please cite the following paper:

Jing Li, Ming Liao, Wei Gao, Yulan He, and Kam-Fai Wong:" Topic Extraction from Microblog Posts Using Conversation Structures", The 54th Annual Meeting of the Association for Computational Linguistics, August 2016, Berlin, Germany.

For the details about the prediction of leader probability, please refer to:

Jing Li, Wei Gao, Zhongyu Wei, Baolin Peng, and Kam-Fai Wong:" Using Content-level Structures for Summarizing Microblog Repost Trees", The 2015 Conference on Empirical Methods in Natural Language Processing, September 2015, Lisboa, Portugal.

If you have any query of the code and data-set, please don't hesitate to send email to lijing@se.cuhk.edu.hk (Jing Li).
