# NLP_Research
This repository will constantly updated some milestone papers I have read and my notes(in English) in Natural Language Processing's subfields. And I will also summarize some basic knowledge (in Chinese) to help to better understand these papers.

* [NLP\_Research](#nlp_research)
  * [Named Entity Recognition](#named-entity-recognition)
    * [Dataset](#dataset)
      * [English](#english)
    * [Milestones](#milestones)
      * [Neural Architectures for Named Entity Recognition](#neural-architectures-for-named-entity-recognition)
  * [Machine Trsanslation](#machine-trsanslation)
    * [Dataset](#dataset-1)
      * [English](#english-1)
    * [Milestones](#milestones-1)
      * [BLEU: a Method for Automatic Evaluation of Machine Translation (TODO)](#bleu-a-method-for-automatic-evaluation-of-machine-translation-todo)
      * [Statistical Phrase\-Based Translation (TODO)](#statistical-phrase-based-translation-todo)
      * [Sequence to Sequence Learning with Neural Networks](#sequence-to-sequence-learning-with-neural-networks)
      * [Neural Machine Translation By Jointly Learning To Align And Translate](#neural-machine-translation-by-jointly-learning-to-align-and-translate)
      * [Attention Is All You Need (TODO)](#attention-is-all-you-need-todo)
    * [Survey](#survey)
      * [Six Challenges for Neural Machine Translation (TODO)](#six-challenges-for-neural-machine-translation-todo)
  * [Pre\-training](#pre-training)
    * [Milestones](#milestones-2)
      * [Efficient Estimation of Word Representations in Vector Space (TODO)](#efficient-estimation-of-word-representations-in-vector-space-todo)
      * [GloVe: Global Vectors for Word Representation (TODO)](#glove-global-vectors-for-word-representation-todo)
  * [基础知识总结](#%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86%E6%80%BB%E7%BB%93)
    * [循环神经网络](#%E5%BE%AA%E7%8E%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C)
    * [Transformer](#transformer)

## Named Entity Recognition
### Dataset
#### English
- [CoNLL 2003 (English)](http://www.aclweb.org/anthology/W03-0419.pdf)
- [Long-tail emerging entities](http://aclweb.org/anthology/W17-4418)
- [Ontonotes v5 (English)](https://catalog.ldc.upenn.edu/docs/LDC2013T19/OntoNotes-Release-5.0.pdf)

> [Click to more details](https://github.com/sebastianruder/NLP-progress/blob/master/english/named_entity_recognition.md)

### Milestones
#### Neural Architectures for Named Entity Recognition  
 Guillaume Lample, Miguel Ballesteros, Sandeep Subramanian, Kazuya Kawakami, Chris Dyer  
 *Carnegie Mellon University, NLP Group of Pompeu Fabra University*  
 *NAACL'16*

 - [Link of Paper (Citation: 957)](https://arxiv.org/abs/1603.01360)
 - [Link of Note](https://adacheng.github.io/paper_note/2019/05/05/Neural-Architectures-for-Named-Entity-Recognition/)

> Reference:  
> 1. __Transition-Based Dependency Parsing with Stack Long Short-Term Memory__  
> Chris Dyer, Miguel Ballesteros, Wang Ling, Austin Matthews, Noah A. Smith  
> *Marianas Labs, NLP Group of Pompeu Fabra University, Carnegie Mellon University*  
> *ACL'15*
> 
>  - [Link of Paper (Citation: 438)](https://arxiv.org/abs/1505.08075)
>  - [Link of Note](https://adacheng.github.io/paper_note/2019/05/05/Transition-Based-Dependency-Parsing-with-Stack-Long-Short-Term-Memory/)

## Machine Trsanslation
### Dataset
#### English
- WMT 2014 EN-DE
- WMT 2014 EN-FR

> [Click to more details](https://github.com/sebastianruder/NLP-progress/blob/master/english/machine_translation.md)

### Milestones
#### BLEU: a Method for Automatic Evaluation of Machine Translation (TODO)
  Kishore Papineni, Salim Roukos, Todd Ward, Weijing Zhu  
 *IBM T.J. Watson Research Center*  
 *ACL'02*

 - [Link of Paper (Citation: 9,095)](https://dl.acm.org/citation.cfm?id=1073135)
 - Link of Note

#### Statistical Phrase-Based Translation (TODO)
  Philipp Koehn, Franz Josef Och, Daniel Marcu  
 *Information Sciences Institute, Department of Computer Science, University of Southern California*  
 *NAACL'03*

 - [Link of Paper (Citation: 3,501)](https://dl.acm.org/citation.cfm?id=1073462)
 - Link of Note

#### Sequence to Sequence Learning with Neural Networks
  Ilya Sutskever, Oriol Vinyals, Quoc V. Le  
 *Google*  
 *NIPS'14*

 - [Link of Paper (Citation: 6,687)](https://arxiv.org/abs/1409.3215)
 - [Link of Note](https://adacheng.github.io/paper_note/2019/06/11/Sequence-to-Sequence-Learning-with-Neural-Networks/)

#### Neural Machine Translation By Jointly Learning To Align And Translate
  Dzmitry Bahdanau, KyungHyun Cho, Yoshua Bengio  
 *Jacobs University Bremen, Universite de Montreal*  
 *ICLR'15*

 - [Link of Paper (Citation: 7,171)](https://arxiv.org/abs/1409.0473)
 - [Link of Note](https://adacheng.github.io/paper_note/2019/06/13/Neural-Machine-Traslation-By-Jointly-Learning-To-Align-And-Translate/)

#### Attention Is All You Need (TODO)
  Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin  
 *Carnegie Mellon University, NLP Group of Pompeu Fabra University*  
 *NIPS'17*

 - [Link of Paper (Citation: 2,028)](https://arxiv.org/abs/1706.03762)
 - Link of Note
 
### Survey
#### Six Challenges for Neural Machine Translation (TODO)
  Philipp Koehn, Rebecca Knowles   
 *Computer Science Department, Johns Hopkins University*  
 *ACL'17*

 - [Link of Paper (Citation: 180)](https://arxiv.org/abs/1706.03872)
 - Link of Note

## Pre-training
### Milestones
#### Efficient Estimation of Word Representations in Vector Space (TODO)
  Tomas Mikolov, Kai Chen, Greg Corrado, Jeffrey Dean  
 *Google*  
 *Computer Science'13*

 - [Link of Paper (Citation: 10,678)](https://arxiv.org/abs/1301.3781)
 - Link of Note

> Reference:  
> 1. __Distributed Representations of Words and Phrases and their Compositionality (TODO)__  
> Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg Corrado, Jeffrey Dean  
> *Google*  
> *NIPS'13*
> 
>  - [Link of Paper (Citation: 13,124)](http://papers.nips.cc/paper/5021-distributed-representations-of-words-andphrases)
>  - [Link of Note]

#### GloVe: Global Vectors for Word Representation (TODO)
  Jeffrey Pennington, Richard Socher, Christopher D. Mannning  
 *Computer Science Department, Stanford University*  
 *EMNLP'14*

 - [Link of Paper (Citation: 7,915)](https://www.aclweb.org/anthology/D14-1162)
 - Link of Note

## 基础知识总结
### 循环神经网络
- [Link of Note](https://github.com/AdaCheng/Research_Notes/blob/master/Notes/%E5%BE%AA%E7%8E%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C/RNN/RNN.md)
### Transformer
- [Link of Note](https://github.com/AdaCheng/Research_Notes/blob/master/Notes/Transformer/Transformer.md)

