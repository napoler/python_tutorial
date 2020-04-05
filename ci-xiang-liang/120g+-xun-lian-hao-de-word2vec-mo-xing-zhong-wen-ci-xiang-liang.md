# 120G+训练好的word2vec模型（中文词向量）



从网上了解到，很多人缺少大语料训练的word2vec模型，在此分享下使用120G+语料训练好的word2vec模型。训练语料：  


* 百度百科800w+条，20G+
* 搜狐新闻400w+条，12G+（数据下载链接见其它博文）
* 小说：90G左右

  
模型参数：

* window=5
* min\_count=5
* size=64
* ps：其它参数见gensim库，执行代码为：Word2Vec\(sentence, window=5, min\_count=5,size=64, workers=4\)

其它相关：

1. 分词词典使用了130w+词典。分词代码：jieba.lcut\(sentence\)，默认使用了HMM识别新词；
2. 剔除了所有非中文字符；
3. 最终得到的词典大小为6115353；
4. 目前只跑了64维的结果，后期更新128维词向量；
5. 模型格式有两种bin和model；



链接: [https://pan.baidu.com/s/1eQEAQJ3wIEHV\_vjR7ihVKA](https://pan.baidu.com/s/1eQEAQJ3wIEHV_vjR7ihVKA) 提取码: bf41 复制这段内容后打开百度网盘手机App，操作更方便哦

