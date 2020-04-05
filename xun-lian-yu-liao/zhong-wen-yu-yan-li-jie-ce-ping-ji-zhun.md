# 中文语言理解测评基准

datasets, baselines, pre-trained models, corpus and leaderboard

中文语言理解测评基准，包括代表性的数据集、基准\(预训练\)模型、语料库、排行榜。

我们会选择一系列有一定代表性的任务对应的数据集，做为我们测试基准的数据集。这些数据集会覆盖不同的任务、数据量、任务难度。

## 中文任务基准测评\(CLUE benchmark\)-排行榜 Leaderboard

**排行榜会定期更新                     数据来源: www.CLUEbenchmark.com**

#### 分类任务\(v1版本,正式版\)

| 模型 | Score | 参数 | AFQMC | TNEWS' | IFLYTEK' | CMNLI | WSC | CSL |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [BERT-base](https://github.com/google-research/bert) | 68.77% | 108M | 73.70% | 56.58% | 60.29% | 79.69% | 62.0% | 80.36% |
| [BERT-wwm-ext](https://github.com/ymcui/Chinese-BERT-wwm) | 70.47% | 108M | 74.07% | 56.84% | 59.43% | 80.42% | 61.1% | 80.63% |
| [ERNIE-base](https://github.com/PaddlePaddle/ERNIE) | 70.55% | 108M | 73.83% | 58.33% | 58.96% | 80.29% | 60.8% | 79.1% |
| [RoBERTa-large](https://github.com/brightmart/roberta_zh) | 72.63% | 334M | 74.02% | 57.86% | 62.55% | 81.70% | 72.7% | 81.36% |
| [XLNet-mid](https://github.com/ymcui/Chinese-PreTrained-XLNet) | 68.65% | 200M | 70.50% | 56.24% | 57.85% | 81.25% | 64.4% | 81.26% |
| [ALBERT-xxlarge](https://github.com/google-research/albert) | 71.04% | 235M | 75.6% | **59.46%** | 62.89% | **83.14%** | 61.54% | **83.63%** |
| [ALBERT-xlarge](https://github.com/google-research/albert) | 68.91% | 60M | 69.96% | 57.36% | 59.50% | 81.13% | 64.34% | 81.20% |
| [ALBERT-large](https://github.com/google-research/albert) | 67.91% | 18M | 74% | 55.16% | 57.00% | 78.77% | 62.24% | 80.30% |
| [ALBERT-base](https://github.com/google-research/albert) | 67.44% | 12M | 72.55% | 55.06% | 56.58% | 77.58% | 64.34% | 78.5% |
| [ALBERT-tiny](https://github.com/brightmart/albert_zh) | 61.92% | **4M** | 69.92% | 53.35% | 48.71% | 70.61% | 58.5% | 74.56% |
| [RoBERTa-wwm-ext](https://github.com/ymcui/Chinese-BERT-wwm) | 71.72% | 108M | 74.04% | 56.94% | 60.31% | 80.51% | 67.8% | 81.0% |
| [RoBERTa-wwm-large](https://github.com/ymcui/Chinese-BERT-wwm) | **73.45%** | 330M | **76.55%** | 58.61% | **62.98%** | 82.12% | **74.6%** | 82.13% |

```text
注：AFQMC:蚂蚁语义相似度(Acc)；TNEWS:文本分类(Acc)；IFLYTEK:长文本分类(Acc); CMNLI: 自然语言推理中文版; 
   COPA: 因果推断; WSC: Winograd模式挑战中文版; CSL: 中国科学文献数据集; Score总分是通过计算6个数据集得分平均值获得；
  '代表对原数据集使用albert_tiny模型筛选后获得，数据集与原数据集不同,从而可能导致在这些数据集上albert_tiny表现略低.
```

#### 阅读理解任务

| 模型 | Score | 参数 | CMRC2018 | CHID | C3 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| [BERT-base](https://github.com/google-research/bert) | 72.71 | 108M | 71.60 | 82.04 | 64.50 |
| [BERT-wwm-ext](https://github.com/ymcui/Chinese-BERT-wwm) | 75.12 | 108M | 73.95 | 82.90 | 68.50 |
| [ERNIE-base](https://github.com/PaddlePaddle/ERNIE) | 73.69 | 108M | 74.7 | 82.28 | 64.10 |
| [RoBERTa-large](https://github.com/brightmart/roberta_zh) | 76.85 | 334M | _**78.50**_ | 84.50 | 67.55 |
| [XLNet-mid](https://github.com/ymcui/Chinese-PreTrained-XLNet) | 72.70 | 209M | 66.95 | 83.47 | 67.68 |
| [ALBERT-base](https://github.com/google-research/albert) | 68.08 | 10M | 72.90 | 71.77 | 59.58 |
| [ALBERT-large](https://github.com/google-research/albert) | 71.51 | 16.5M | 75.95 | 74.18 | 64.41 |
| [ALBERT-xlarge](https://github.com/google-research/albert) | 75.73 | 57.5M | 76.30 | 80.57 | 70.32 |
| [ALBERT-xxlarge](https://github.com/google-research/albert) | 77.19 | 221M | 75.15 | 83.15 | 73.28 |
| [ALBERT-tiny](https://github.com/brightmart/albert_zh) | 49.05 | 1.8M | 53.35 | 43.53 | 50.26 |
| [RoBERTa-wwm-ext](https://github.com/ymcui/Chinese-BERT-wwm) | 75.11 | 108M | 75.20 | 83.62 | 66.50 |
| [RoBERTa-wwm-large](https://github.com/ymcui/Chinese-BERT-wwm) | _**79.05**_ | 330M | 77.95 | _**85.37**_ | _**73.82**_ |

DRCD、CMRC2018: 繁体、简体抽取式阅读理解\(F1, EM\)；CHID: 成语多分类阅读理解\(Acc\)；C3: 多选中文阅读理解\(Acc\)；Score总分是通过计算3个数据集得分平均值获得。

注：阅读理解上述指标中F1和EM共存的情况下，取EM为最终指标。CMRC2018结果为CLUE专用独立测试集。

## 一键运行.基线模型与代码 Baseline with codes

```text
使用方式：
1、克隆项目 
   git clone https://github.com/CLUEbenchmark/CLUE.git
2、进入到相应的目录
   分类任务  
       例如：
       cd CLUE/baselines/models/bert
       cd CLUE/baselines/models_pytorch/classifier_pytorch
   或阅读理解任务：
       cd CLUE/baselines/models_pytorch/mrc_pytorch
3、运行对应任务的脚本(GPU方式): 会自动下载模型和任务数据并开始运行。
   bash run_classifier_xxx.sh
   如运行 bash run_classifier_iflytek.sh 会开始iflytek任务的训练  
4、tpu使用方式(可选)  
    cd CLUE/baselines/models/bert/tpu  
    sh run_classifier_tnews.sh即可测试tnews任务（注意更换里面的gs路径和tpu ip）。数据和模型会自动下载和上传。

    cd CLUE/baselines/models/roberta/tpu  
    sh run_classifier_tiny.sh即可运行所有分类任务（注意更换里面的路径,模型地址和tpu ip）  
```

### 运行环境

tensorflow 1.12 /cuda 9.0 /cudnn7.0

### 工具包 Toolkit

运行方式：

```text
pip install PyCLUE 
cd PyCLUE/examples/classifications
python3 run_clue_task.py
```

支持10个任务、9大模型、自定义任务，见 [PyCLUE toolkit](https://github.com/CLUEbenchmark/PyCLUE)

### 生成提交文件

```text
分类任务: 
    在CLUE/baselines/models/bert目录下执行
    sh run_classifier_xxx.sh predict 
    即可在output_dir下得到相应的提交文件json格式结果xxx_prdict.json
```

或见[代码实现](https://github.com/CLUEbenchmark/CLUE/blob/master/baselines/models/bert/run_classifier.py#L932-L951)

```text
阅读理解任务:
     在CLUE/baselines/models_pytorch/mrc_pytorch目录下执行
     test_mrc.py
     具体参数和使用方法可见对应的run_mrc_xxx.sh
​    
```

[提交样例下载](https://storage.googleapis.com/cluebenchmark/tasks/clue_submit_examples.zip)

## 测评系统 Leaderboard

测评入口：[我要提交](http://www.CLUEbenchmark.com) ![](https://github.com/CLUEbenchmark/CLUE/blob/master/resources/img/CLUEbenchmark.jpg)

## 语料库\(CLUECorpus2020\)：语言建模、预训练或生成型任务

Corpus for Langauge Modelling, Pre-training, Generating tasks

可用于语言建模、预训练或生成型任务等，数据量超过14G，近4000个定义良好的txt文件、50亿个字。主要部分来自于[nlp\_chinese\_corpus项目](https://github.com/brightmart/nlp_chinese_corpus)

当前语料库按照【预训练格式】处理，内含有多个文件夹；每个文件夹有许多不超过4M大小的小文件，文件格式符合预训练格式：每句话一行，文档间空行隔开。

包含如下子语料库（总共14G语料）：

1、[新闻语料 news2016zh\_corpus](https://pan.baidu.com/s/195M7H5w3N8shYlqCjVL0_Q): 8G语料，分成两个上下两部分，总共有2000个小文件。 密码:mzlk

2、[社区互动-语料 webText2019zh\_corpus](https://pan.baidu.com/s/1Vk2PihMiZNmWvA2agPb1iA)：3G语料，包含3G文本，总共有900多个小文件。 密码:qvlq

3、[维基百科-语料 wiki2019zh\_corpus](https://pan.baidu.com/s/1XrM-x70PY4JEb0xCoB_mUw)：1.1G左右文本，包含300左右小文件。 密码:rja4

4、[评论数据-语料 comments2019zh\_corpus](https://pan.baidu.com/s/16cPwCcPduMNGdRSuILhEuQ)：2.3G左右文本，共784个小文件，包括点评评论547个、亚马逊评论227个，合并[ChineseNLPCorpus](https://github.com/InsaneLife/ChineseNLPCorpus)的多个评论数据，清洗、格式转换、拆分成小文件。 密码:5kwk

这些语料，你可以通过上面这两个项目，清洗数据并做格式转换获得；

你也可以通过邮件申请（chineseGLUE\#163.com）获得单个项目的语料，告知单位或学校、姓名、语料用途；

如需获得ChineseGLUE项目下的所有语料，需成为ChineseGLUE组织成员，并完成一个（小）任务。

## CLUE benchmark的定位 Vision

为更好的服务中文语言理解、任务和产业界，做为通用语言模型测评的补充，通过完善中文语言理解基础设施的方式来促进中文语言模型的发展

## 数据集介绍与下载 Introduction of datasets

[提交样例下载](https://storage.googleapis.com/cluebenchmark/tasks/clue_submit_examples.zip)

**1. AFQMC 蚂蚁金融语义相似度 Ant Financial  Question Matching Corpus**

```text
     数据量：训练集（34334）验证集（4316）测试集（3861）
     例子：
     {"sentence1": "双十一花呗提额在哪", "sentence2": "里可以提花呗额度", "label": "0"}
     每一条数据有三个属性，从前往后分别是 句子1，句子2，句子相似度标签。其中label标签，1 表示sentence1和sentence2的含义类似，0表示两个句子的含义不同。
```

 [AFQMC'数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/afqmc_public.zip)

**2.TNEWS' 今日头条中文新闻（短文本）分类 Short Text Classificaiton for News**

该数据集来自今日头条的新闻版块，共提取了15个类别的新闻，包括旅游，教育，金融，军事等。

```text
     数据量：训练集(53,360)，验证集(10,000)，测试集(10,000)
     例子：
     {"label": "102", "label_des": "news_entertainment", "sentence": "江疏影甜甜圈自拍，迷之角度竟这么好看，美吸引一切事物"}
     每一条数据有三个属性，从前往后分别是 分类ID，分类名称，新闻字符串（仅含标题）。
```

 [TNEWS'数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/tnews_public.zip)

**3.IFLYTEK' 长文本分类 Long Text classification**

该数据集共有1.7万多条关于app应用描述的长文本标注数据，包含和日常生活相关的各类应用主题，共119个类别："打车":0,"地图导航":1,"免费WIFI":2,"租车":3,….,"女性":115,"经营":116,"收款":117,"其他":118\(分别用0-118表示\)。

```text
    数据量：训练集(12,133)，验证集(2,599)，测试集(2,600)
    例子：
    {"label": "110", "label_des": "社区超市", "sentence": "朴朴快送超市创立于2016年，专注于打造移动端30分钟即时配送一站式购物平台，商品品类包含水果、蔬菜、肉禽蛋奶、海鲜水产、粮油调味、酒水饮料、休闲食品、日用品、外卖等。朴朴公司希望能以全新的商业模式，更高效快捷的仓储配送模式，致力于成为更快、更好、更多、更省的在线零售平台，带给消费者更好的消费体验，同时推动中国食品安全进程，成为一家让社会尊敬的互联网公司。,朴朴一下，又好又快,1.配送时间提示更加清晰友好2.保障用户隐私的一些优化3.其他提高使用体验的调整4.修复了一些已知bug"}
    每一条数据有三个属性，从前往后分别是 类别ID，类别名称，文本内容。
```

 [IFLYTEK'数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/iflytek_public.zip)

**4.CMNLI 语言推理任务 Chinese Multi-Genre NLI**

CMNLI数据由两部分组成：XNLI和MNLI。数据来自于fiction，telephone，travel，government，slate等，对原始MNLI数据和XNLI数据进行了中英文转化，保留原始训练集，合并XNLI中的dev和MNLI中的matched作为CMNLI的dev，合并XNLI中的test和MNLI中的mismatched作为CMNLI的test，并打乱顺序。该数据集可用于判断给定的两个句子之间属于蕴涵、中立、矛盾关系。

```text
    数据量：train(391,782)，dev(12,426)，test(13,880)
    例子：
    {"sentence1": "新的权利已经足够好了", "sentence2": "每个人都很喜欢最新的福利", "label": "neutral"}
    每一条数据有三个属性，从前往后分别是 句子1，句子2，蕴含关系标签。其中label标签有三种：neutral，entailment，contradiction。
```

 [CMNLI数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/cmnli_public.zip)

**5. WSC Winograd模式挑战中文版  The Winograd Schema Challenge,Chinese Version**

威诺格拉德模式挑战赛是图灵测试的一个变种，旨在判定AI系统的常识推理能力。参与挑战的计算机程序需要回答一种特殊但简易的常识问题：代词消歧问题，即对给定的名词和代词判断是否指代一致。

```text
数据量：训练集(532)，验证集(104)，测试集(143) 
例子：
{"target": 
    {"span2_index": 28, 
     "span1_index": 0, 
     "span1_text": "马克", 
     "span2_text": "他"
    }, 
     "idx": 0, 
     "label": "false", 
     "text": "马克告诉皮特许多关于他自己的谎言，皮特也把这些谎言写进了他的书里。他应该多怀疑。"
}
    其中label标签，true表示指代一致，false表示指代不一致。
```

 [WSC数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/wsc_public.zip)

**6. CSL 论文关键词识别 Keyword Recognition**

[中文科技文献数据集\(CSL\)](https://github.com/P01son6415/chinese-scientific-literature-dataset)取自中文论文摘要及其关键词，论文选自部分中文社会科学和自然科学核心期刊。 使用tf-idf生成伪造关键词与论文真实关键词混合，构造摘要-关键词对，任务目标是根据摘要判断关键词是否全部为真实关键词。

```text
    数据量：训练集(20,000)，验证集(3,000)，测试集(3,000)
    例子： 
    {"id": 1, "abst": "为解决传统均匀FFT波束形成算法引起的3维声呐成像分辨率降低的问题,该文提出分区域FFT波束形成算法.远场条件下,以保证成像分辨率为约束条件,以划分数量最少为目标,采用遗传算法作为优化手段将成像区域划分为多个区域.在每个区域内选取一个波束方向,获得每一个接收阵元收到该方向回波时的解调输出,以此为原始数据在该区域内进行传统均匀FFT波束形成.对FFT计算过程进行优化,降低新算法的计算量,使其满足3维成像声呐实时性的要求.仿真与实验结果表明,采用分区域FFT波束形成算法的成像分辨率较传统均匀FFT波束形成算法有显著提高,且满足实时性要求.", "keyword": ["水声学", "FFT", "波束形成", "3维成像声呐"], "label": "1"}
    每一条数据有四个属性，从前往后分别是 数据ID，论文摘要，关键词，真假标签。
```

 [CSL数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/csl_public.zip)

**7.CMRC2018 简体中文阅读理解任务 Reading Comprehension for Simplified Chinese**

[https://hfl-rc.github.io/cmrc2018/](https://hfl-rc.github.io/cmrc2018/)

```text
数据量：训练集(短文数2,403，问题数10,142)，试验集(短文数256，问题数1,002)，开发集(短文数848，问题数3,219)  
例子：
{
  "version": "1.0",
  "data": [
    {
        "title": "傻钱策略",
        "context_id": "TRIAL_0",
        "context_text": "工商协进会报告，12月消费者信心上升到78.1，明显高于11月的72。另据《华尔街日报》报道，2013年是1995年以来美国股市表现最好的一年。这一年里，投资美国股市的明智做法是追着“傻钱”跑。所谓的“傻钱”策略，其实就是买入并持有美国股票这样的普通组合。这个策略要比对冲基金和其它专业投资者使用的更为复杂的投资方法效果好得多。",
        "qas":[
                {
                "query_id": "TRIAL_0_QUERY_0",
                "query_text": "什么是傻钱策略？",
                "answers": [
                     "所谓的“傻钱”策略，其实就是买入并持有美国股票这样的普通组合",
                     "其实就是买入并持有美国股票这样的普通组合",
                     "买入并持有美国股票这样的普通组合"
                    ]
                },
                {
                "query_id": "TRIAL_0_QUERY_1",
                "query_text": "12月的消费者信心指数是多少？",
                "answers": [
                    "78.1",
                    "78.1",
                    "78.1"
                    ]
                },
                {
                "query_id": "TRIAL_0_QUERY_2",
                "query_text": "消费者信心指数由什么机构发布？",
                "answers": [
                    "工商协进会",
                    "工商协进会",
                    "工商协进会"
                    ]
                }
            ]
        }
    ]
}
```

 [CMRC2018数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/cmrc2018_public.zip)

**8.DRCD 繁体阅读理解任务 Reading Comprehension for Traditional Chinese**

台達閱讀理解資料集 Delta Reading Comprehension Dataset \(DRCD\)\([https://github.com/DRCKnowledgeTeam/DRCD](https://github.com/DRCKnowledgeTeam/DRCD)\) 屬於通用領域繁體中文機器閱讀理解資料集。 本資料集期望成為適用於遷移學習之標準中文閱讀理解資料集。

```text
数据量：训练集(8,016个段落，26,936个问题)，验证集(1,000个段落，3,524个问题)，测试集(1,000个段落，3,493个问题)  
例子：
{
  "version": "1.3",
  "data": [
    {
      "title": "基督新教",
      "id": "2128",
      "paragraphs": [
        {
          "context": "基督新教與天主教均繼承普世教會歷史上許多傳統教義，如三位一體、聖經作為上帝的啟示、原罪、認罪、最後審判等等，但有別於天主教和東正教，新教在行政上沒有單一組織架構或領導，而且在教義上強調因信稱義、信徒皆祭司， 以聖經作為最高權威，亦因此否定以教宗為首的聖統制、拒絕天主教教條中關於聖傳與聖經具同等地位的教導。新教各宗派間教義不盡相同，但一致認同五個唯獨：唯獨恩典：人的靈魂得拯救唯獨是神的恩典，是上帝送給人的禮物。唯獨信心：人唯獨藉信心接受神的赦罪、拯救。唯獨基督：作為人類的代罪羔羊，耶穌基督是人與上帝之間唯一的調解者。唯獨聖經：唯有聖經是信仰的終極權威。唯獨上帝的榮耀：唯獨上帝配得讚美、榮耀",
          "id": "2128-2",
          "qas": [
            {
              "id": "2128-2-1",
              "question": "新教在教義上強調信徒皆祭司以及什麼樣的理念?",
              "answers": [
                {
                  "id": "1",
                  "text": "因信稱義",
                  "answer_start": 92
                }
              ]
            },
            {
              "id": "2128-2-2",
              "question": "哪本經典為新教的最高權威?",
              "answers": [
                {
                  "id": "1",
                  "text": "聖經",
                  "answer_start": 105
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

数据格式和squad相同，如果使用简体中文模型进行评测的时候可以将其繁转简\(本项目已提供\)  [DRCD2018数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/drcd_public.zip)

**9.ChID 成语阅读理解填空 Chinese IDiom Dataset for Cloze Test**

[https://arxiv.org/abs/1906.01265](https://arxiv.org/abs/1906.01265)  
成语完形填空，文中多处成语被mask，候选项中包含了近义的成语。

```text
    数据量：训练集(84,709)，验证集(3,218)，测试集(3,231)
    例子：
    {
      "content": [
        # 文段0
        "……在热火22年的历史中，他们已经100次让对手得分在80以下，他们在这100次中都取得了胜利，今天他们希望能#idiom000378#再进一步。", 
        # 文段1
        "在轻舟发展过程之中，是和业内众多企业那样走相似的发展模式，去#idiom000379#？还是迎难而上，另走一条与众不同之路。诚然，#idiom000380#远比随大流更辛苦，更磨难，更充满风险。但是有一条道理却是显而易见的：那就是水往低处流，随波逐流，永远都只会越走越低。只有创新，只有发展科技，才能强大自己。", 
        # 文段2
        "最近十年间，虚拟货币的发展可谓#idiom000381#。美国著名经济学家林顿·拉鲁什曾预言：到2050年，基于网络的虚拟货币将在某种程度上得到官方承认，成为能够流通的货币。现在看来，这一断言似乎还嫌过于保守……", 
        # 文段3
        "“平时很少能看到这么多老照片，这次图片展把新旧照片对比展示，令人印象深刻。”现场一位参观者对笔者表示，大多数生活在北京的人都能感受到这个城市#idiom000382#的变化，但很少有人能具体说出这些变化，这次的图片展按照区域发展划分，展示了丰富的信息，让人形象感受到了60年来北京的变化和发展。", 
        # 文段4
        "从今天大盘的走势看，市场的热点在反复的炒作之中，概念股的炒作#idiom000383#，权重股走势较为稳健，大盘今日早盘的震荡可以看作是多头关前的蓄势行为。对于后市，大盘今日蓄势震荡后，明日将会在权重和题材股的带领下亮剑冲关。再创反弹新高无悬念。", 
        # 文段5
        "……其中，更有某纸媒借尤小刚之口指出“根据广电总局的这项要求，2009年的荧屏将很难出现#idiom000384#的情况，很多已经制作好的非主旋律题材电视剧想在卫视的黄金时段播出，只能等到2010年了……"],
      "candidates": [
        "百尺竿头", 
        "随波逐流", 
        "方兴未艾", 
        "身体力行", 
        "一日千里", 
        "三十而立", 
        "逆水行舟", 
        "日新月异", 
        "百花齐放", 
        "沧海一粟"
      ]
    }
```

 [CHID数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/chid_public.zip)

**10.C3 中文多选阅读理解 Multiple-Choice Chinese Machine Reading Comprehension**

[https://arxiv.org/abs/1904.09679](https://arxiv.org/abs/1904.09679)  
中文多选阅读理解数据集，包含对话和长文等混合类型数据集。训练和验证集中的d,m分别代表对话、多种文本类型混合。

```text
    数据量：训练集(11,869)，验证集(3,816)，测试集(3,892)
    例子：
    [
      [
        "男：你今天晚上有时间吗?我们一起去看电影吧?",
        "女：你喜欢恐怖片和爱情片，但是我喜欢喜剧片，科幻片一般。所以……"
      ],
      [
       {
        "question": "女的最喜欢哪种电影?",
        "choice": [
         "恐怖片",
         "爱情片",
         "喜剧片",
         "科幻片"
        ],
        "answer": "喜剧片"
       }
      ],
    "25-35"
    ],
    [
      [
       "男：足球比赛是明天上午八点开始吧?",
       "女：因为天气不好，比赛改到后天下午三点了。"
      ],
      [
       {
        "question": "根据对话，可以知道什么?",
        "choice": [
         "今天天气不好",
         "比赛时间变了",
         "校长忘了时间"
        ],
        "answer": "比赛时间变了"
       }
      ],
    "31-109"
    ]
```

 [C3数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/c3_public.zip)

**11. 诊断集 CLUE\_diagnostics test\_set**

诊断集，用于评估不同模型在9种语言学家总结的中文语言现象上的表现

使用在CMNLI上训练过的模型，直接预测在这个诊断集上的结果，提交格式和CMNLI一致，在排行榜详情页可以看到结果

[diagnostics数据集下载](https://storage.googleapis.com/cluebenchmark/tasks/clue_diagnostics_public.zip)

**更多数据集添加中，Comming soon!**

如果你有定义良好的数据集并愿意为社区做贡献，请与我们取得联系 ChineseGLUE\#163.com

**数据集整体下载**

[整体下载 Comining Soon]()最近几天，会添加中

或使用命令：wget 

Data filter method

## 难样本数据集筛选方法

为了增加模型区分度和增大数据集难度，我们采用**k折交叉验证**的方式对v0版本的数据集进行过滤，最终得到v1版本。

```text
具体步骤：
1.将特定任务的数据集集中在一起，同时选择一个基准测试模型（如AlbertTiny）
2.将数据集均匀分成k份；每次选择其中1份当验证集，剩下的都作为训练集，训练基准模型并在验证集上测试、保留预测结果
3.重复步骤二k次，让每一份数据都有机会当验证集，过完整个数据集
4.将k份验证集的预测结果合并；保留其中预测错误的样本（可以认为是较难的数据），并删除一部分预测正确的样本。最后重新划分出训练集、验证集、测试集
5.如果希望进一步筛选难样本，重复步骤2-4即可
```

Notes：

```text
1.k一般选择4-6
2.难样本，是指在交叉验证过程中模型预测错误的样本，也是我们希望尽可能保留的样本。模型预测正确的样本最终会被优先排除一部分
```

## 内容体系 Contents

Language Understanding Evaluation benchmark for Chinese\(ChineseGLUE\) got ideas from GLUE, which is a collection of

resources for training, evaluating, and analyzing natural language understanding systems. ChineseGLUE consists of:

**1）中文任务的基准测试，覆盖多个不同程度的语言任务**

A benchmark of several sentence or sentence pair language understanding tasks. Currently the datasets used in these tasks are come from public. We will include datasets with private test set before the end of 2019.

**2）公开的排行榜 Leaderboard**

A public leaderboard for tracking performance. You will able to submit your prediction files on these tasks, each task will be evaluated and scored, a final score will also be available.

**3）基线模型，包含开始的代码、预训练模型  Baselines with code**

baselines for ChineseGLUE tasks. baselines will be available in TensorFlow,PyTorch,Keras and PaddlePaddle.

**4）语料库，用于语言建模、预训练或生成型任务  Corpus**

A huge amount of raw corpus for pre-train or language modeling research purpose. It will contains around 10G raw corpus in 2019;

In the first half year of 2020, it will include at least 30G raw corpus; By the end of 2020, we will include enough raw corpus, such as 100G, so big enough that you will need no more raw corpus for general purpose language modeling. You can use it for general purpose or domain adaption, or even for text generating. when you use for domain adaption, you will able to select corpus you are interested in.

**5）工具包 toolkit**

An easy to use toolkit that can run specific task or model with one line of code. You can easily change configuration, task or model.

**6\) 技术报告**

Techical report with details

Why do we need a benchmark for Chinese lanague understand evaluation?

## 为什么我们需要一个中文任务的基准测试？

首先，中文是一个大语种，有其自身的特定、大量的应用。

```text
如中文使用人数近14亿，是联合国官方语言之一，产业界有大量的的朋友在做中文的任务。
中文是象形文字，有文字图形；字与字之间没有分隔符，不同的分词(分字或词)会影响下游任务。
```

其次，相对于英文的数据集，中文的公开可用的数据集还比较少。

```text
 很多数据集是非公开的或缺失基准测评的；多数的论文描述的模型是在英文数据集上做的测试和评估，那么对于中文效果如何？不得而知。
```

再次，语言理解发展到当前阶段，预训练模型极大的促进了自然语言理解。

```text
 不同的预训练模型相继产生，但不少最先进(state of the art)的模型，并没有官方的中文的版本，也没有对这些预训练模型在不同任务上的公开测试，
 导致技术的发展和应用还有不少距离，或者说技术应用上的滞后。
```

那么，如果有一个中文任务的基准测试，包含一批大众能广泛使用和测评的数据集、适用中文任务的特点、能紧跟当前世界技术的发展，

```text
 能缓解当前中文任务的一些问题，并促进相关应用的发展。
```

## 各任务详细对比

Evaluation of Dataset for Different Models

#### AFQMC 蚂蚁语义相似度 Ant Semantic Similarity \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| ALBERT-xxlarge | - | - | - |
| ALBERT-tiny | 69.13% | 69.92% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| BERT-base | 74.16% | 73.70% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| BERT-wwm-ext-base | 73.74% | 74.07% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| ERNIE-base | 74.88% | 73.83% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-large | 73.32% | 74.02% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| XLNet-mid | 70.73% | 70.50% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-ext | 74.30% | 74.04% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-large-ext | 74.92% | 76.55% | batch\_size=16, length=128, epoch=3 lr=2e-5 |

#### TNEWS' 头条新闻分类 Toutiao News Classification \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| ALBERT-xxlarge | - | - | - |
| ALBERT-tiny | 53.55% | 53.35% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| BERT-base | 56.09% | 56.58% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| BERT-wwm-ext-base | 56.77% | 56.86% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| ERNIE-base | 58.24% | 58.33% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-large | 57.95% | 57.84% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| XLNet-mid | 56.09% | 56.24% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-ext | 57.51% | 56.94% | batch\_size=16, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-large-ext | 58.32% | 58.61% | batch\_size=16, length=128, epoch=3 lr=2e-5 |

#### IFLYTEK' 长文本分类 Long Text Classification \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| ALBERT-xlarge | - | - | batch=32, length=128, epoch=3 lr=2e-5 |
| ALBERT-tiny | 48.76 | 48.71 | batch=32, length=128, epoch=10 lr=2e-5 |
| BERT-base | 60.37 | 60.29 | batch=32, length=128, epoch=3 lr=2e-5 |
| BERT-wwm-ext-base | 59.88 | 59.43 | batch=32, length=128, epoch=3 lr=2e-5 |
| ERNIE-base | 59.52 | 58.96 | batch=32, length=128, epoch=3 lr=2e-5 |
| RoBERTa-large | 62.6 | 62.55 | batch=24, length=128, epoch=3 lr=2e-5 |
| XLNet-mid | 57.72 | 57.85 | batch=32, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-ext | 60.8 | 60.31 | batch=32, length=128, epoch=3 lr=2e-5 |
| RoBERTa-wwm-large-ext | **62.75** | **62.98** | batch=24, length=128, epoch=3 lr=2e-5 |

#### CMNLI 中文自然语言推理 Chinese Multi-Genre NLI \(Accuracy\)：

| 模型 | 开发集 \(dev %\) | 测试集（test %\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| BERT-base | 79.47 | 79.69 | batch=64, length=128, epoch=2 lr=3e-5 |
| BERT-wwm-ext-base | 80.92 | 80.42 | batch=64, length=128, epoch=2 lr=3e-5 |
| ERNIE-base | 80.37 | 80.29 | batch=64, length=128, epoch=2 lr=3e-5 |
| ALBERT-xxlarge | - | - | - |
| ALBERT-tiny | 70.26 | 70.61 | batch=64, length=128, epoch=2 lr=3e-5 |
| RoBERTa-large | 82.40 | 81.70 | batch=64, length=128, epoch=2 lr=3e-5 |
| xlnet-mid | 82.21 | 81.25 | batch=64, length=128, epoch=2 lr=3e-5 |
| RoBERTa-wwm-ext | 80.70 | 80.51 | batch=64, length=128, epoch=2 lr=3e-5 |
| RoBERTa-wwm-large-ext | _**83.20**_ | _**82.12**_ | batch=64, length=128, epoch=2 lr=3e-5 |

注：ALBERT-xlarge，在XNLI任务上训练暂时还存在有问题

#### WSC Winograd模式挑战中文版  The Winograd Schema Challenge,Chinese Version：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| ALBERT-xxlarge | - | - | - |
| ALBERT-tiny | 57.7\(52.9\) | 58.5\(52.1\) | lr=1e-4, batch\_size=8, length=128, epoch=50 |
| BERT-base | 59.6（56.7\) | 62.0（57.9） | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| BERT-wwm-ext-base | 59.4\(56.7\) | 61.1\(56.2\) | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| ERNIE-base | 58.1\(54.9\) | 60.8\(55.9\) | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| RoBERTa-large | 68.6\(58.7\) | 72.7\(63.6\) | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| XLNet-mid | 60.9\(56.8） | 64.4\(57.3） | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| RoBERTa-wwm-ext | 67.2\(57.7\) | 67.8\(63.5\) | lr=2e-5, batch\_size=8, length=128, epoch=50 |
| RoBERTa-wwm-large-ext | 69.7\(64.5\) | 74.6\(69.4\) | lr=2e-5, batch\_size=8, length=128, epoch=50 |

#### CSL 关键词识别  Keyword Recognition \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| ALBERT-xlarge | 80.23 | 80.29 | batch\_size=16, length=128, epoch=2, lr=5e-6 |
| ALBERT-tiny | 74.36 | 74.56 | batch\_size=4, length=256, epoch=5, lr=1e-5 |
| BERT-base | 79.63 | 80.23 | batch\_size=4, length=256, epoch=5, lr=1e-5 |
| BERT-wwm-ext-base | 80.60 | 81.00 | batch\_size=4, length=256, epoch=5, lr=1e-5 |
| ERNIE-base | 79.43 | 79.10 | batch\_size=4, length=256, epoch=5, lr=1e-5 |
| RoBERTa-large | 81.87 | 81.36 | batch\_size=4, length=256, epoch=5, lr=5e-6 |
| XLNet-mid | 82.06 | 81.26 | batch\_size=4, length=256, epoch=3, lr=1e-5 |
| RoBERTa-wwm-ext | 80.67 | 80.63 | batch\_size=4, length=256, epoch=5, lr=1e-5 |
| RoBERTa-wwm-large-ext | 82.17 | 82.13 | batch\_size=4, length=256, epoch=5, lr=1e-5 |

#### DRCD 繁体阅读理解 Reading Comprehension for Traditional Chinese \(F1, EM\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| BERT-base | F1:92.30 EM:86.60 | F1:91.46 EM:85.49 | batch=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| BERT-wwm-ext-base | F1:93.27 EM:88.00 | F1:92.63 EM:87.15 | batch=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| ERNIE-base | F1:92.78 EM:86.85 | F1:92.01 EM:86.03 | batch=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| ALBERT-large | F1:93.90 EM:88.88 | F1:93.06 EM:87.52 | batch=32, length=512, epoch=3, lr=2e-5, warmup=0.05 |
| ALBERT-xlarge | F1:94.63 EM:89.68 | F1:94.70 EM:89.78 | batch\_size=32, length=512, epoch=3, lr=2.5e-5, warmup=0.06 |
| ALBERT-xxlarge | F1:93.69 EM:89.97 | F1:94.62 EM:89.67 | batch\_size=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| ALBERT-tiny | F1:81.51 EM:71.61 | F1:80.67 EM:70.08 | batch=32, length=512, epoch=3, lr=2e-4, warmup=0.1 |
| RoBERTa-large | F1:94.93 EM:90.11 | F1:94.25 EM:89.35 | batch=32, length=256, epoch=2, lr=3e-5, warmup=0.1 |
| xlnet-mid | F1:92.08 EM:84.40 | F1:91.44 EM:83.28 | batch=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| RoBERTa-wwm-ext | F1:94.26 EM:89.29 | F1:93.53 EM:88.12 | batch=32, length=512, epoch=2, lr=3e-5, warmup=0.1 |
| RoBERTa-wwm-large-ext | _**F1:95.32 EM:90.54**_ | _**F1:95.06 EM:90.70**_ | batch=32, length=512, epoch=2, lr=2.5e-5, warmup=0.1 |

#### CMRC2018 阅读理解 Reading Comprehension for Simplified Chinese \(F1, EM\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| BERT-base | F1:85.48 EM:64.77 | F1:88.10 EM:71.60 | batch=32, length=512, epoch=2 lr=3e-5 warmup=0.1 |
| BERT-wwm-ext-base | F1:86.68 EM:66.96 | F1:89.62 EM:73.95 | batch=32, length=512, epoch=2 lr=3e-5 warmup=0.1 |
| ERNIE-base | F1:87.30 EM:66.89 | F1:90.57 EM:74.70 | batch=32, length=512, epoch=2 lr=3e-5 warmup=0.1 |
| ALBERT-base | F1:85.86 EM:64.76 | F1:89.66 EM:72.90 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| ALBERT-large | F1:87.36 EM:67.31 | F1:90.81 EM:75.95 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| ALBERT-xlarge | F1:88.99 EM:69.08 | F1:92.09 EM:76.30 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| ALBERT-xxlarge | F1:87.47 EM:66.43 | F1:90.77 EM:75.15 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| ALBERT-tiny | F1:73.95 EM:48.31 | F1:76.21 EM:53.35 | batch=32, epoch3, length=512, lr=2e-4, warmup=0.1 |
| RoBERTa-large | F1:88.61 EM:69.94 | _**F1:92.04 EM:78.50**_ | batch=32, epoch2, length=256, lr=3e-5, warmup=0.1 |
| xlnet-mid | F1:85.63 EM:65.31 | F1:86.11 EM:66.95 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| RoBERTa-wwm-ext | F1:87.28 EM:67.89 | F1:90.41 EM:75.20 | batch=32, epoch2, length=512, lr=3e-5, warmup=0.1 |
| RoBERTa-wwm-large-ext | _**F1:89.42 EM:70.59**_ | F1:92.11 EM:77.95 | batch=32, epoch2, length=512, lr=2.5e-5, warmup=0.1 |

注: 现在榜上数据为cmrc2018的2k测试集子集作为测试，而并非cmrc2018官方完整测试集。如需完整测试cmrc2018阅读理解数据集仍需通过cmrc2018平台提交\([https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647\)。](https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647%29。)

#### CHID 成语阅读理解填空 Chinese IDiom Dataset for Cloze Test \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| BERT-base | 82.20 | 82.04 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| BERT-wwm-ext-base | 83.36 | 82.9 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ERNIE-base | 82.46 | 82.28 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ALBERT-base | 70.99 | 71.77 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ALBERT-large | 75.10 | 74.18 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ALBERT-xlarge | 81.20 | 80.57 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ALBERT-xxlarge | 83.61 | 83.15 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| ALBERT-tiny | 43.47 | 43.53 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| RoBERTa-large | 85.31 | 84.50 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| xlnet-mid | 83.76 | 83.47 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| RoBERTa-wwm-ext | 83.78 | 83.62 | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |
| RoBERTa-wwm-large-ext | _**85.81**_ | _**85.37**_ | batch=24, length=64, epoch=3, lr=2e-5, warmup=0.06 |

#### C3 成语阅读理解填空 中文多选阅读理解 Multiple-Choice Chinese Machine Reading Comprehension \(Accuracy\)：

| 模型 | 开发集（dev\) | 测试集（test\) | 训练参数 |
| :---: | :---: | :---: | :---: |
| BERT-base | 65.70 | 64.50 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| BERT-wwm-ext-base | 67.80 | 68.50 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ERNIE-base | 65.50 | 64.10 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ALBERT-base | 60.43 | 59.58 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ALBERT-large | 64.07 | 64.41 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ALBERT-xlarge | 69.75 | 70.32 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ALBERT-xxlarge | 73.66 | 73.28 | batch=16, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| ALBERT-tiny | 50.58 | 50.26 | batch=32, length=512, epoch=8, lr=5e-5, warmup=0.1 |
| RoBERTa-large | 67.79 | 67.55 | batch=24, length=256, epoch=8, lr=2e-5, warmup=0.1 |
| xlnet-mid | 66.17 | 67.68 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| RoBERTa-wwm-ext | 67.06 | 66.50 | batch=24, length=512, epoch=8, lr=2e-5, warmup=0.1 |
| RoBERTa-wwm-large-ext | _**74.48**_ | _**73.82**_ | batch=16, length=512, epoch=8, lr=2e-5, warmup=0.1 |

## 成为ChineseGLUE组织的创始成员 Members

**你将可以 Benefits：**

1、成功中国第一个中文任务基准测评的创始会员

2、能与其他专业人士共同贡献力量，促进中文自然语言处理事业的发展

3、参与部分工作后，获得已经清洗并预训练的后的、与英文wiki & bookCorpus同等量级、大规模的预训练语料，用于研究目的。

4、优先使用state of the art的中文预训练模型，包括各种体验版或未公开版本

**如何参与 How to join with us：**

发送邮件 chineseGLUE\#163.com，简要介绍你自己、背景、工作或研究方向、你的组织、在哪方面可以为社区贡献力量，我们评估后会与你取得联系你。

## 任务清单 TODO LIST

1、搜集、挖掘1个有代表性的数据集，一般为分类或句子对任务 \(需要额外5个数据集\)

2、阅读理解任务转化成句子对任务（如线索与问题或答案），并做测评，数据应拆分成训练、验证和测试集。

3、基线模型baselises在特定任务模型的训练、预测的方法和脚本\(支持PyTorch、Keras\)；

4、对当前主流模型（如bert/bert\_wwm\_ext/roberta/albert/ernie/ernie2.0等），结合ChineseGLUE的数据集，做准确率测试。

如： XLNet-mid在LCQMC数据集上做测试

5、是否还有没有参与测评的模型？

**其他**

6、排行榜landing页

7、介绍中文语言理解测评基准\(ChineseGLUE\)

8、测评系统主要功能开发

## Timeline 时间计划:

2019-10-20 to 2019-12-31: beta version of ChineseGLUE

2020.1.1 to 2020-12-31: official version of ChineseGLUE

2021.1.1 to 2021-12-31: super version of ChineseGLUE

## Contribution 贡献你的力量，从今天开始

Share your data set with community or make a contribution today! Just send email to chineseGLUE\#163.com,

or join QQ group: 836811304

#### Research supported with Cloud TPUs from Google's TensorFlow Research Cloud \(TFRC\)

## Cite Us:

```text
@misc{CLUEbenchmark_2020,
  title={CLUE benchmark},
  author={anonymous},
  year={2020},
  publisher={Github},
  journal={GitHub repository},
  howpublished={\url{https://https://github.com/CLUEbenchmark/CLUE}},
}
```

## Reference:

1、[GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding](https://openreview.net/pdf?id=rJ4km2R5t7)

2、[SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems](https://w4ngatang.github.io/static/papers/superglue.pdf)

4、[XNLI: Evaluating Cross-lingual Sentence Representations](https://arxiv.org/pdf/1809.05053.pdf)

5、[TNES: toutiao-text-classfication-dataset](https://github.com/fate233/toutiao-text-classfication-dataset)

6、[nlp\_chinese\_corpus: 大规模中文自然语言处理语料 Large Scale Chinese Corpus for NLP](https://github.com/brightmart/nlp_chinese_corpus)

7、[ChineseNLPCorpus](https://github.com/InsaneLife/ChineseNLPCorpus)

8、[ALBERT: A Lite BERT For Self-Supervised Learning Of Language Representations](https://arxiv.org/abs/1909.11942)

9、[BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/pdf/1810.04805.pdf)

10、[RoBERTa: A Robustly Optimized BERT Pretraining Approach](https://arxiv.org/pdf/1907.11692.pdf)
