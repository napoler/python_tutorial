---
description: 使用bert微调提取实体，描述这些信息。
---

# 文本标记tkitMarker\_bert

{% embed url="https://github.com/napoler/tkitMarker\_bert" %}

使用bert微调提取实体，描述这些信息。

## 安装

```text
pip install tkitMarker_bert
```

## 测试

```text
from tkitMarker_bert import Marker

text="柯基犬是一个小短腿"
word="柯基犬"
#加载预测描述
pred=Marker(model_path="./model")
model,tokenizer=pred.load_model()
pall=pred.pre(word,text,model,tokenizer)
print(word,pall)
>>>柯基犬 ['是一个小短腿']

```

## 训练数据标记

[https://github.com/napoler/tmark\_Description](https://github.com/napoler/tmark_Description)

## 更多返回





