# albert\_zh 中文模型 tf版本和pytorch

### [https://github.com/brightmart/albert\_zh](https://github.com/brightmart/albert_zh)

### 模型下载 Download Pre-trained Models of Chinese

1、[albert\_tiny\_zh](https://storage.googleapis.com/albert_zh/albert_tiny.zip), [albert\_tiny\_zh\(训练更久，累积学习20亿个样本\)](https://storage.googleapis.com/albert_zh/albert_tiny_489k.zip)，文件大小16M、参数为4M

```text
训练和推理预测速度提升约10倍，精度基本保留，模型大小为bert的1/25；语义相似度数据集LCQMC测试集上达到85.4%，相比bert_base仅下降1.5个点。

lcqmc训练使用如下参数： --max_seq_length=128 --train_batch_size=64   --learning_rate=1e-4   --num_train_epochs=5 

albert_tiny使用同样的大规模中文语料数据，层数仅为4层、hidden size等向量维度大幅减少; 尝试使用如下学习率来获得更好效果：{2e-5, 6e-5, 1e-4} 

【使用场景】任务相对比较简单一些或实时性要求高的任务，如语义相似度等句子对任务、分类任务；比较难的任务如阅读理解等，可以使用其他大模型。

 例如，可以使用[Tensorflow Lite](https://www.tensorflow.org/lite)在移动端进行部署，本文[随后](#use_tflite)针对这一点进行了介绍，包括如何把模型转换成Tensorflow Lite格式和对其进行性能测试等。
 
 一键运行albert_tiny_zh(linux,lcqmc任务)：
 1) git clone https://github.com/brightmart/albert_zh
 2) cd albert_zh
 3) bash run_classifier_lcqmc.sh
```

1.1、[albert\_tiny\_google\_zh\(累积学习10亿个样本,google版本\)](https://storage.googleapis.com/albert_zh/albert_tiny_zh_google.zip)，模型大小16M、性能与albert\_tiny\_zh一致

1.2、[albert\_small\_google\_zh\(累积学习10亿个样本,google版本\)](https://storage.googleapis.com/albert_zh/albert_small_zh_google.zip)，

```text
 速度比bert_base快4倍；LCQMC测试集上比Bert下降仅0.9个点；去掉adam后模型大小18.5M；使用方法，见 #下游任务 Fine-tuning on Downstream Task     
```

2、[albert\_large\_zh](https://storage.googleapis.com/albert_zh/albert_large_zh.zip),参数量，层数24，文件大小为64M

```text
参数量和模型大小为bert_base的六分之一；在口语化描述相似性数据集LCQMC的测试集上相比bert_base上升0.2个点
```

3、[albert\_base\_zh\(额外训练了1.5亿个实例即 36k steps \* batch\_size 4096\)](https://storage.googleapis.com/albert_zh/albert_base_zh_additional_36k_steps.zip); [albert\_base\_zh\(小模型体验版\)](https://storage.googleapis.com/albert_zh/albert_base_zh.zip), 参数量12M, 层数12，大小为40M

```text
参数量为bert_base的十分之一，模型大小也十分之一；在口语化描述相似性数据集LCQMC的测试集上相比bert_base下降约0.6~1个点；
相比未预训练，albert_base提升14个点
```

4、[albert\_xlarge\_zh\_177k ](https://storage.googleapis.com/albert_zh/albert_xlarge_zh_177k.zip); [albert\_xlarge\_zh\_183k\(优先尝试\)](https://storage.googleapis.com/albert_zh/albert_xlarge_zh_183k.zip)参数量，层数24，文件大小为230M

```text
参数量和模型大小为bert_base的二分之一；需要一张大的显卡；完整测试对比将后续添加；batch_size不能太小，否则可能影响精度
```

#### 快速加载

依托于[Huggingface-Transformers 2.2.2](https://github.com/huggingface/transformers)，可轻松调用以上模型。

```text
tokenizer = AutoTokenizer.from_pretrained("MODEL_NAME")
model = AutoModel.from_pretrained("MODEL_NAME")
```

其中`MODEL_NAME`对应列表如下：

| 模型名 | MODEL\_NAME |
| :--- | :--- |
| albert\_tiny\_google\_zh | voidful/albert\_chinese\_tiny |
| albert\_small\_google\_zh | voidful/albert\_chinese\_small |
| albert\_base\_zh \(from google\) | voidful/albert\_chinese\_base |
| albert\_large\_zh \(from google\) | voidful/albert\_chinese\_large |
| albert\_xlarge\_zh \(from google\) | voidful/albert\_chinese\_xlarge |
| albert\_xxlarge\_zh \(from google\) | voidful/albert\_chinese\_xxlarge |

更多通过transformers使用albert的[示例](https://huggingface.co/models?search=albert_chinese)





