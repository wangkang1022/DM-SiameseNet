# DM-SiameseNet in PyTorch


## Prerequisites
- scipy==1.2.1
- numpy==1.17.0
- matplotlib==3.1.2
- opencv_python==4.1.2.30
- torch==1.2.0
- torchvision==0.4.0
- tqdm==4.60.0
- Pillow==8.2.0
- h5py==2.10.0
- Python 3
- GPU + CUDA CuDNN

## Getting Started
### Installation

- Clone this repo:
```bash
https://github.com/wangkang1022/DM-SiameseNet
```

- Install dependencies.

### Datasets 
- [百度网盘(提取码：yr1w)](https://pan.baidu.com/share/init?surl=M3jFo2OI5GTOpytxgtO1qA). <br>
Thanks [LibFewShot: A Comprehensive Library for Few-shot Learning](https://arxiv.org/abs/2109.04898) for providing the Birds-200-2011, Standford Cars, Standford Dogs, miniImageNet and tieredImageNet.

###  miniImageNet, tieredImageNet, Birds-200-2011, Standford Cars, Standford Dogs Few-shot Classification
- Train a 5-way 1-shot or 5-shot model based on Conv64F :
```bash
python DN4_Train_5way1shot.py --dataset_dir ./datasets/miniImageNet --data_name miniImageNet
or
python DN4_Train_5way5shot.py --dataset_dir ./datasets/miniImageNet --data_name miniImageNet
```
- Test the model (specify the dataset_dir, basemodel, and data_name first):
```bash
python DN4_Test_5way1shot.py --resume ./results/DN4_miniImageNet_Conv64F_5Way_1Shot_K3/model_best.pth.tar --basemodel Conv64F
or
python DN4_Test_5way1shot.py --resume ./results/DN4_miniImageNet_Conv64F_5Way_5Shot_K3/model_best.pth.tar --basemodel Conv64F
```

- The results on the miniImageNet dataset (If you modify neighbor_k or lr, you may get better results in some cases): 


## References
Our code is based on Li's contribution. Specifically, except for our core design, Siamese network , everything else （e.g. backbone, dataset, evaluation standards, hyper-parameters）are built on and integrated in https://github.com/WenbinLee/DN4.

##Contact
- 897893203@qq.com
