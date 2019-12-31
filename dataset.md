
# dataset

| Name                                                         | Cascades    | Avg. Length | Nodes   | Edges      | Is On Graph | From                                                         | Related Paper                                                |
| ------------------------------------------------------------ | ----------- | ----------- | ------- | ---------- | ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Twitter([FOREST](https://github.com/albertyang33/FOREST/tree/master/data/twitter), [deepDiffuse](https://github.com/raihan2108/deep-diffuse/tree/master/data/twitter), [topoLSTM](https://github.com/vwz/topolstm/tree/master/datasets/twitter)) |             |             |         |            | No          | [The simple rules of social contagion](https://www.nature.com/articles/srep04343#Sec4) | [FOREST](http://nlp.csai.tsinghua.edu.cn/~yangcheng/publications/ijcai19.pdf),  [NDM](http://nlp.csai.tsinghua.edu.cn/~yangcheng/publications/tkde19.pdf), [TopoLSTM](https://arxiv.org/pdf/1711.10162.pdf), [DeepDiffuse](http://people.cs.vt.edu/ramakris/papers/deepdiffuse-icdm2018.pdf) |
| Douban                                                       | 10,602      | 27.14       | 23,123  | 348,280    | No          | Comsoc: Adaptive transfer of user behaviors over composite social network. | FOREST,                                                      |
| [Memetracker](http://www.memetracker.org/)                   |             |             |         |            | No          | Meme-tracking and the dynamics of the news cycle             | FOREST, NDM, TopoLSTM, DeepDiffuse, [Hi-DAN](https://pdfs.semanticscholar.org/a8a7/353a42b90d2f43504783dc81ff28c11a9da5.pdf) |
| Lastfm                                                       | 23802       | 7.66        | 982     | 506,582    | No          | Music recommendation and discovery in the ` long tail        | NDM                                                          |
| Irvine                                                       | 471         | 13.63       | 540     | 62,605     | No          | “Clustering in weighted networks,” Social networks           | NMD                                                          |
| Digg([TopoLSTM](https://github.com/vwz/topolstm/tree/master/datasets/digg)) | 3,553       | 30.0        |         |            |             | [“Social dynamics of digg,](https://epjdatascience.springeropen.com/articles/10.1140/epjds5#Sec2) | TopoLSTM, DeepDiffuse                                        |
| Twitter                                                      | about 30000 |             | 354,634 | 27,929,863 |             | DeepCas: an End-to-end Predictor of Information Cascades     | [DeepCas](https://arxiv.org/pdf/1611.05373.pdf)              |
| [AMiner](https://www.aminer.cn/citation)                     | about 30000 |             | 131,415 | 842,542    |             | DeepCas: an End-to-end Predictor of Information Cascades     | DeepCas                                                      |
| Twitter                                                      |             |             |         |            |             | Virality prediction and community structure in social networks. | Hi-DAN                                                       |
| Weibo                                                        |             |             |         |            |             | Social influence locality for modeling retweeting behaviors. | Hi-DAN                                                       |
|                                                              |             |             |         |            |             |                                                              |                                                              |



## Memetracker

Meme在不同网站的传播，meme当做是消息，网站当做节点。以时间先后构造的cascade。无网络。

## Digg

用户对3553篇文章进行投票，时间顺序构成cascade。可以有好友网络。

## Twitter1

推文里提到的URL当做信息，在不同用户间传播。“无法判断谁影响的谁”，隐含的意思也是按时间构造的？

## Twitter2

Deepcas自己构造的，转发和@构造网络，推文当做传播的信息，在用户间转发。不清楚是不是按时间，还是有真正的A转发B。

## AMiner

论文引用，DeepCas里，1992-2002被引关系构造网络，后面的年份构造数据集，cascade是一篇文章，作者以及引用它的人构成(作者-引用人1-引用人2...)。感觉是以时间先后构成的。AMiner本身能构造出图上传播的数据集。
