# CJC

## Introduction

- From the paper "SICM: A Supervised-based Identification and Classification Model for Chinese Jargons Using Feature Adapter Enhanced BERT".

- CJC is the first labeled dataset of Chinese jargons, which divides jargons into seven categories, including 'Drug', 'Gambling', 'Pornography', 'Violence', 'Fraud', 'Hacking' and 'Others'.

- Using the BIOES tagging scheme.

- The data comes from Chinese underground forums on the darknet where cybercriminal activities are active.

- CJC contains 33,668 sentences, including 19,675 sentences containing jargons and 13,993 normal sentences. A total of 45,079 jargons were labeled, including 1,796 unduplicated jargons. The details are as follows:

  |  Category   | #Sentences | #Jargons | #Unduplicated jargons |            Example of jargons            |
  | :---------: | :--------: | :------: | :-------------------: | :--------------------------------------: |
  |    Drug     |   1,936    |  3,920   |          225          |          叶子(leaf), 猪肉(pork)          |
  |  Gambling   |   1,831    |  3,713   |          239          |     菠菜(spinach), 搏彩(fight color)     |
  | Pornography |   4,132    |  10,560  |          362          |   果体(fruit body), 狼友(wolf friend)    |
  |  Violence   |   1,456    |  3,469   |          203          |     气狗(air dog), 秃鹰(bald eagle)      |
  |    Fraud    |   4,284    |  10,320  |          381          | 轨道料(rail material), 裸条(bare strip)  |
  |   Hacking   |   4,138    |  8,147   |          341          | 蜜獾(Mellivora capensis), 轰炸机(bomber) |
  |   Others    |   2,998    |  4,860   |          47           |        梯子(ladder), 洋葱(onion)         |



## Labeling Strategy

- The term is a normal word which has a normal meaning, but when the context is considered, it clearly means something else associated with cybercriminal acts (e.g., "猪肉" (pork), "水果" (fruit)).

- The term is a new word that has never been seen before, and judging from the context, it clearly has a Implicit meaning and is related to cybercrime (e.g., "洗信人" (letter washer), "轨道料'' (rail material)).



## Data Sources

- First, we adopt the unlabeled data of the darknet published [here](https://github.com/KL4MVP/Chinese-Jargon-Detection/tree/master/dataset).

- Then, In order to balance the amount of data in different crime categories, we supplement data from additional Chinese darknet forums:

  暗网中文担保交易市场: http://xxxxxxxxnu2x2zvszlwa4j7qzu3dop7asuthzjkziq2xni7odzifhkid.onion

  自由国度: http://khwfgj4bixwmdve42iwb2fd2bhty5nowr45rz6lmfpk4nwjbre5owwqd.onion

  长安不夜城: http://cabyceogpsji73sske5nvo45mdrkbz4m3qd3iommf3zaaa6izg3j2cqd.onion

