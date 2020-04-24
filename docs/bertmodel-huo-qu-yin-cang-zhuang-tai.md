# BertModel 获取隐藏状态

[https://huggingface.co/transformers/model\_doc/bert.html\#bertmodel](https://huggingface.co/transformers/model_doc/bert.html#bertmodel)

```text
from transformers import BertModel, BertTokenizer
import torch

tokenizer = BertTokenizer.from_pretrained('bert-base-chinese')
model = BertModel.from_pretrained('bert-base-chinese')

input_ids = torch.tensor(tokenizer.encode("Hello, my dog is cute", add_special_tokens=True)).unsqueeze(0)  # Batch size 1
outputs = model(input_ids)

last_hidden_states = outputs[0]  # The last hidden-state is the first element of the output tuple
```

