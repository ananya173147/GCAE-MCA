# Introduction  
A reproduction of the paper "Aspect Based Sentiment Analysis with Gated Convolutional Networks" (ACL 2018) using PyTorch    

```
@inproceedings{DBLP:conf/acl/LiX18,
  author    = {Wei Xue and Tao Li},
  title     = {Aspect Based Sentiment Analysis with Gated Convolutional Networks},
  booktitle = {Proceedings of the 56th Annual Meeting of the Association for Computational
               Linguistics, {ACL} 2018, Melbourne, Australia, July 15-20, 2018, Volume
               1: Long Papers},
  pages     = {2514--2523},
  year      = {2018},
  crossref  = {DBLP:conf/acl/2018-1},
  url       = {https://aclanthology.info/papers/P18-1234/p18-1234},
  timestamp = {Thu, 12 Jul 2018 14:15:56 +0200},
  biburl    = {https://dblp.org/rec/bib/conf/acl/LiX18},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```

# Requirements  
tensorboardX 2.4  
sacremoses 0.0.46   
torchtext 0.5.0   
pytorch 1.9.0  
simplejson 3.17.5  


# Run
Download the glove word vectors and change the path in train.py in the line 33  
If you run the code in Linux, you should change the path of train.py in line 102, from r"\\" to r"/"  

## ATSA Task
python train.py -atsa  -lr 5e-3 -batch_size 32 -model gcae_atsa -atsa_data rest -epochs 6  
python train.py -atsa  -lr 5e-3 -batch_size 32 -model gcae_atsa -atsa_data laptop -epochs 5  

## ACSA Task

python train.py -lr 1e-2 -batch_size 32 -model gcae_acsa -acsa_data 2014  -epochs 5    
python train.py -lr 1e-2 -batch_size 32 -model gcae_acsa -acsa_data large  -epochs 13    

# Reproduction-Experiment Result  

**ACSA Task:**

![ACSA Task](https://user-images.githubusercontent.com/59045952/141677190-90dfafb5-0ab2-434d-bae2-bd973954ee0b.png)


**ATSA Task:**

![ATSA Task](https://user-images.githubusercontent.com/59045952/141677207-91bdcf1c-8c3a-4d76-b301-a78bba9705d0.png)

# References

- https://github.com/wxue004cs/GCAE (Authors' code)
- https://github.com/SinclairCoder/GCAE-Reproduce
- https://github.com/songyouwei/ABSA-PyTorch
- Maria Pontiki, Dimitrios Galanis, John Pavlopoulos, Haris Papageorgiou, Ion Androutsopoulos, and Suresh Manandhar. 2014. Semeval-2014 task 4: Aspect based sentiment analysis. In SemEval@COLING, pages 27–35, Stroudsburg, PA, USA. Association for Computational Linguistics. 
- Chen, Y., Fan, H., Xu, B., Yan, Z., Kalantidis, Y., Rohrbach, M., Yan, S., & Feng, J. (2019). Drop an Octave: Reducing Spatial Redundancy in Convolutional Neural Networks With Octave Convolution. 2019 IEEE/CVF International Conference on Computer Vision (ICCV), 3434-3443.
- Hu, J., Shen, L., Albanie, S., Sun, G., & Wu, E. (2020). Squeeze-and-Excitation Networks. IEEE Transactions on Pattern Analysis and Machine Intelligence, 42, 2011-2023.


