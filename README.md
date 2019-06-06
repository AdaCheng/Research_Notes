# NLP_Research
This repository will constantly updated some milestone papers I have read and my notes(in English) in Natural Language Processing's subfields. And I will also summarize some basic knowledge (in Chinese) to help to better understand these papers.

* [NLP\_Research](#nlp_research)
  * [Named Entity Recognition](#named-entity-recognition)
    * [Dateset &amp; state\-of\-the\-art](#dateset--state-of-the-art)
      * [CoNLL 2003 (English)](#conll-2003-english)
    * [Milestones](#milestones)
      * [Neural Architectures for Named Entity Recognition](#neural-architectures-for-named-entity-recognition)
  * [Machine Trsanslation](#machine-trsanslation)
    * [Dateet &amp; state\-of\-the\-art](#dateet--state-of-the-art)
      * [WMT 2014 EN\-DE](#wmt-2014-en-de)
    * [Milestones](#milestones-1)
      * [BLEU: a Method for Automatic Evaluation of Machine Translation(TODO)](#bleu-a-method-for-automatic-evaluation-of-machine-translationtodo)
      * [Sequence to Sequence Learning with Neural Networks(TODO)](#sequence-to-sequence-learning-with-neural-networkstodo)
      * [Neural Machine Translation By Jointly Learning To Align And Translate(TODO)](#neural-machine-translation-by-jointly-learning-to-align-and-translatetodo)
      * [Attention Is All You Need](#attention-is-all-you-need)
  * [基础知识总结](#%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86%E6%80%BB%E7%BB%93)
    * [循环神经网络](#%E5%BE%AA%E7%8E%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C)
    * [Transformer](#transformer)
  * [Reference](#reference)

## Named Entity Recognition
### Dateset & state-of-the-art
#### CoNLL 2003 (English)
The [CoNLL 2003 NER task](http://www.aclweb.org/anthology/W03-0419.pdf) consists of newswire text from the Reuters RCV1 
corpus tagged with four different entity types (PER, LOC, ORG, MISC). Models are evaluated based on span-based F1 on the test set. ♦ used both the train and development splits for training.

| Model           | F1  |  Paper / Source | Code |
| ------------- | :-----:| --- | --- |
| CNN Large + fine-tune (Baevski et al., 2019) | 93.5 | [Cloze-driven Pretraining of Self-attention Networks](https://arxiv.org/pdf/1903.07785.pdf) | |
| Flair embeddings (Akbik et al., 2018)♦ | 93.09 | [Contextual String Embeddings for Sequence Labeling](https://drive.google.com/file/d/17yVpFA7MmXaQFTe-HDpZuqw9fJlmzg56/view) | [Flair framework](https://github.com/zalandoresearch/flair)
| BERT Large (Devlin et al., 2018) | 92.8 | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) | |
| CVT + Multi-Task (Clark et al., 2018) | 92.61 | [Semi-Supervised Sequence Modeling with Cross-View Training](https://arxiv.org/abs/1809.08370) | [Official](https://github.com/tensorflow/models/tree/master/research/cvt_text) |
| BERT Base (Devlin et al., 2018) | 92.4 | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) | |
| BiLSTM-CRF+ELMo (Peters et al., 2018) | 92.22 | [Deep contextualized word representations](https://arxiv.org/abs/1802.05365) | [AllenNLP Project](https://allennlp.org/elmo) [AllenNLP GitHub](https://github.com/allenai/allennlp) |
| Peters et al. (2017) ♦| 91.93 | [Semi-supervised sequence tagging with bidirectional language models](https://arxiv.org/abs/1705.00108) | |
| CRF + AutoEncoder (Wu et al., 2018) | 91.87 | [Evaluating the Utility of Hand-crafted Features in Sequence Labelling](http://aclweb.org/anthology/D18-1310) | [Official](https://github.com/minghao-wu/CRF-AE) | 
| Bi-LSTM-CRF + Lexical Features (Ghaddar and Langlais 2018) | 91.73 | [Robust Lexical Features for Improved Neural Network Named-Entity Recognition](https://arxiv.org/pdf/1806.03489.pdf) | [Official](https://github.com/ghaddarAbs/NER-with-LS) |
| Chiu and Nichols (2016) ♦| 91.62 | [Named entity recognition with bidirectional LSTM-CNNs](https://arxiv.org/abs/1511.08308) | |
| HSCRF (Ye and Ling, 2018)| 91.38 | [Hybrid semi-Markov CRF for Neural Sequence Labeling](http://aclweb.org/anthology/P18-2038) | [HSCRF](https://github.com/ZhixiuYe/HSCRF-pytorch) |
| IXA pipes (Agerri and Rigau 2016) | 91.36 | [Robust multilingual Named Entity Recognition with shallow semi-supervised features](https://doi.org/10.1016/j.artint.2016.05.003)| [Official](https://github.com/ixa-ehu/ixa-pipe-nerc)|
| NCRF++ (Yang and Zhang, 2018)| 91.35 | [NCRF++: An Open-source Neural Sequence Labeling Toolkit](http://www.aclweb.org/anthology/P18-4013) | [NCRF++](https://github.com/jiesutd/NCRFpp) |
| LM-LSTM-CRF (Liu et al., 2018)| 91.24 | [Empowering Character-aware Sequence Labeling with Task-Aware Neural Language Model](https://arxiv.org/pdf/1709.04109.pdf) | [LM-LSTM-CRF](https://github.com/LiyuanLucasLiu/LM-LSTM-CRF) |
| Yang et al. (2017) ♦| 91.26 | [Transfer Learning for Sequence Tagging with Hierarchical Recurrent Networks](https://arxiv.org/abs/1703.06345) | |
| Ma and Hovy (2016) | 91.21 | [End-to-end Sequence Labeling via Bi-directional LSTM-CNNs-CRF](https://arxiv.org/abs/1603.01354) | |
| LSTM-CRF (Lample et al., 2016) | 90.94 | [Neural Architectures for Named Entity Recognition](https://arxiv.org/abs/1603.01360) | |

### Milestones
#### Neural Architectures for Named Entity Recognition  
 Guillaume Lample, Miguel Ballesteros, Sandeep Subramanian, Kazuya Kawakami, Chris Dyer  
 *Carnegie Mellon University, NLP Group of Pompeu Fabra University*  
 *NAACL'16*

 - [Link of Paper](https://arxiv.org/abs/1603.01360)
 - [Link of Note](https://github.com/AdaCheng/Research_Notes/blob/master/Papers/Neural%20Architectures%20for%20Named%20Entity%20Recognition/Neural%20Architectures%20for%20Named%20Entity%20Recognition.md)

> Reference:  
> 1. __Transition-Based Dependency Parsing with Stack Long Short-Term Memory__  
> Chris Dyer, Miguel Ballesteros, Wang Ling, Austin Matthews, Noah A. Smith  
> *Marianas Labs, NLP Group of Pompeu Fabra University, Carnegie Mellon University*  
> *ACL'15*
> 
>  - [Link of Paper](https://arxiv.org/abs/1505.08075)
>  - [Link of Note](https://github.com/AdaCheng/Research_Notes/blob/master/Papers/Neural%20Architectures%20for%20Named%20Entity%20Recognition/Transition-Based%20Dependency%20Parsing%20with%20Stack%20Long%20Short-Term%20Memory/Transition-Based%20Dependency%20Parsing%20with%20Stack%20Long%20Short-Term%20Memory.md)

## Machine Trsanslation
### Dateet & state-of-the-art
#### WMT 2014 EN-DE
Models are evaluated on the English-German dataset of the Ninth Workshop on Statistical Machine Translation (WMT 2014) based
on BLEU.

| Model           | BLEU  |  Paper / Source |
| ------------- | :-----:| --- |
| Transformer Big + BT (Edunov et al., 2018) | 35.0 | [Understanding Back-Translation at Scale](https://arxiv.org/pdf/1808.09381.pdf) |
| DeepL | 33.3 | [DeepL Press release](https://www.deepl.com/press.html) |
| DynamicConv (Wu et al., 2019)| 29.7 | [Pay Less Attention With Lightweight and Dynamic Convolutions](https://arxiv.org/abs/1901.10430) |
| Transformer Big (Ott et al., 2018) | 29.3 | [Scaling Neural Machine Translation](https://arxiv.org/abs/1806.00187) |
| RNMT+ (Chen et al., 2018) | 28.5* | [The Best of Both Worlds: Combining Recent Advances in Neural Machine Translation](https://arxiv.org/abs/1804.09849) |
| Transformer Big (Vaswani et al., 2017) | 28.4 | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) |
| Transformer Base (Vaswani et al., 2017) | 27.3 | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) |
| MoE (Shazeer et al., 2017) | 26.03 | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538) |
| ConvS2S (Gehring et al., 2017) | 25.16 | [Convolutional Sequence to Sequence Learning](https://arxiv.org/abs/1705.03122) | 

### Milestones
#### BLEU: a Method for Automatic Evaluation of Machine Translation(TODO)
  Kishore Papineni, Salim Roukos, Todd Ward, Weijing Zhu  
 *IBM T.J. Watson Research Center*  
 *ACL'02*

 - [Link of Paper](https://dl.acm.org/citation.cfm?id=1073135)
 - [Link of Note]()

#### Sequence to Sequence Learning with Neural Networks(TODO)
  Ilya Sutskever, Oriol Vinyals, Quoc V. Le  
 *Google*  
 *NIPS'14*

 - [Link of Paper](https://arxiv.org/abs/1409.3215)
 - [Link of Note]()

#### Neural Machine Translation By Jointly Learning To Align And Translate(TODO)
  Dzmitry Bahdanau, KyungHyun Cho, Yoshua Bengio  
 *Jacobs University Bremen, Universite de Montreal*  
 *ICLR'15*

 - [Link of Paper](https://arxiv.org/abs/1409.0473)
 - [Link of Note]()

#### Attention Is All You Need   
  Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin  
 *Carnegie Mellon University, NLP Group of Pompeu Fabra University*  
 *NIPS'17*

 - [Link of Paper](https://arxiv.org/abs/1706.03762)
 - [Link of Note](https://github.com/AdaCheng/Research_Notes/blob/master/Notes/Transformer/Transformer.md)
 
## 基础知识总结
### [循环神经网络](https://github.com/AdaCheng/Research_Notes/blob/master/Notes/%E5%BE%AA%E7%8E%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C/RNN/RNN.md)
### [Transformer](https://github.com/AdaCheng/Research_Notes/blob/master/Notes/Transformer/Transformer.md)

## Reference
> [NLP-progress](https://github.com/sebastianruder/NLP-progress/) by Sebastian Ruder
