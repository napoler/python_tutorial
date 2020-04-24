# 搜索关键词进行聚类



```text
#搜索关键词进行聚类

from albertk import *
model,tokenizer=load_albert("data/albert_tiny")
keyword=input("输入关键词：")
# keyword="边境牧羊犬智商"
klist=run_search_sent(keyword,20,tokenizer,model)
print(klist)

```

