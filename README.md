# Hierarchical Attention Networks

A minimal PyTorch implementation of Hierarchical Attention Networks (HANs) for document classification.

Supported features:
- Mini-batch training with CUDA
- Lookup, CNNs, RNNs and/or self-attention in the embedding layer

## Usage

Training data should be formatted as below:
```
sentence
...
sentence
label

sentence
...
sentence
label

...
```

To prepare data:
```
python3 prepare.py training_data
```

To train:
```
python3 train.py model char_to_idx word_to_idx tag_to_idx training_data.csv (validation_data) num_epoch
```

To predict:
```
python3 predict.py model.epochN char_to_idx word_to_idx tag_to_idx test_data
```

To evaluate:
```
python3 evaluate.py model.epochN char_to_idx word_to_idx tag_to_idx test_data
```

## References

Zichao Yang, Diyi Yang, Chris Dyer, Xiaodong He, Alex Smola, Eduard Hovy. 2016. [Hierarchical Attention Networks for Document Classification.](https://www.aclweb.org/anthology/N16-1174) In NAACL-HLT.
