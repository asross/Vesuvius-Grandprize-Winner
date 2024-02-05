# Vesuvius Grandprize Winning Solution
![Vesuvius Challenge GP Solution](pictures/logo.png)

The Repository contains the First Place Vesuvius Grand Prize solution. 
This repository is part of the First Place Grand Prize Submission to the Vesuvius Challenge 2023 from Youssef Nader, Luke Farritor and Julian Schilliger.

<!-- <img align="center" width="60" height="60" src="pictures/ThaumatoAnakalyptor.png">  -->
## Automatic Segmentation <img align="center" width="60" height="60" src="pictures/ThaumatoAnakalyptor.png"> 
Check out the automatic segmentation pipeline ThaumatoAnakalyptor of our winning Grand Prize submission by Julian Schiliger. 
[ThaumatoAnakalyptor](https://github.com/schillij95/ThaumatoAnakalyptor/tree/main) performs in full 3D and is also capable of segmenting in very mushy and twisted scroll regions.

# Ink Detection Overview<img align="center" width="60" height="60" src="pictures/logo.png"> :
Our final canonical model was a timesformer small architecture with divided space-time attention. 
The dataset underwent expansion and cleaning rounds to increase accuracy of the labels and become as accurate as possible, approximately 15 rounds were performed between the first letters and final solution. 
Our solution also consisted of 2 other architectures, Resnet3D-101 with pretrained weights, I3D with non-local block and maxpooling. 

Our implementation uses `torch`, `torch-lightning`,the [`timesformer-pytorch`](https://github.com/lucidrains/TimeSformer-pytorch) and [`3D-ResNets-PyTorch`](https://github.com/kenshohara/3D-ResNets-PyTorch/blob/master/models/resnet.py). 


# 🚀 Get Started


To install this project, run:

```bash
pip install -r requirements
#to download the segments from the server
./download.sh
#propagates the inklabels into the respective segment folders for training
python prepare.py
```







