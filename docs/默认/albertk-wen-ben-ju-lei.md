# albertk文本聚类

### 安装

```text
pip install albertk
```

### 使用

pytorch模型下载

{% embed url="https://www.kaggle.com/terrychanorg/pytorch-albert-zh" %}

{% embed url="https://www.kaggle.com/terrychanorg/albert-tiny-pytorch" %}



```text
from albertk import *
model,tokenizer=load_albert("data/albert_tiny")


keyword=input("输入关键词：")
# keyword="边境牧羊犬智商"
klist=run_search_sent(keyword,tokenizer,model)
print(klist)
```

