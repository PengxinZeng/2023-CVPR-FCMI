

<div align="center">


### PyTorch implementation for 

  ## Deep Fair Clustering via Maximizing and Minimizing Mutual Information: Theory, Algorithm and Metric 

CVPR 2023
  
[[Paper]](https://arxiv.org/pdf/2209.12396)                [[Discussion]](https://github.com/PengxinZeng/2023-CVPR-FCMI/issues)  [[More Information]](https://github.com/PengxinZeng?tab=repositories)
</div>

## Introduction

### FCMI framework
<img src="https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/Fig2.png"  width="740"  />

## Requirements

- Python 3.9
- PyTorch 1.11.0
- [faiss](https://anaconda.org/pytorch/faiss-gpu)
```
conda install -c pytorch faiss-gpu
```
  
## Datasets

### Color Reverse MNIST, Office-31, MTFL, and MNIST-USPS  

We follow [DFC](https://openaccess.thecvf.com/content_CVPR_2020/papers/Li_Deep_Fair_Clustering_for_Visual_Learning_CVPR_2020_paper.pdf) to obtain datasets.

### HAR 
We follow [DFDC](https://arxiv.org/pdf/2105.14146.pdf) to obtain dataset.



## Training

Modify the ```./Utils/PathPresettingOperator.get_dataset_path```, then train the model(s):
```train
# Color Reverse MNIST
python main.py --dataset ReverseMNIST --seed 0  
  
# Office-31  
python main.py --dataset Office --seed 0  
  
# MTFL  
python main.py --dataset MTFL --seed 9116  
  
# HAR  
python main.py --dataset HAR --seed 9116  
  
# MNIST-USPS  
python main.py --dataset MNISTUSPS --seed 9116  
```

## Model Zoo
The pre-trained models are available here:
| Dataset | Model | Results |
|--|--|--|
| Color Reverse MNIST | [Model](https://drive.google.com/drive/folders/1pfw4YCGkYP1XupGw-GNBip_dNaqBCODl?usp=share_link) | [Results](https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/TrainRevMnist.txt) |
| Office-31 | [Model](https://drive.google.com/drive/folders/1pfw4YCGkYP1XupGw-GNBip_dNaqBCODl?usp=share_link) | [Results](https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/TrainOffice.txt) |
| MTFL | [Model](https://drive.google.com/drive/folders/1pfw4YCGkYP1XupGw-GNBip_dNaqBCODl?usp=share_link) | [Results](https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/TrainMTFL.txt) |
| HAR | [Model](https://drive.google.com/drive/folders/1pfw4YCGkYP1XupGw-GNBip_dNaqBCODl?usp=share_link) | [Results](https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/TrainHAR.txt) |
| MNIST-USPS | [Model](https://drive.google.com/drive/folders/1pfw4YCGkYP1XupGw-GNBip_dNaqBCODl?usp=share_link) | [Results](https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/TrainRevMnist.txt) |

Download the models, then:
```
python main.py --dataset dataset --seed seed --resume PathToYourModel
```

## Experiment Results:
<img src="https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/Tab1.png"  width="740"  />
<img src="https://github.com/PengxinZeng/2023-CVPR-FCMI/blob/main/FigVisual.png"  width="600"  />


## Citation

If FCMI is useful for your research, please cite the following paper:

```
@inproceedings{zeng2023deep,
  title={Deep Fair Clustering via Maximizing and Minimizing Mutual Information: Theory, Algorithm and Metric},
  author={Zeng, Pengxin and Li, Yunfan and Hu, Peng and Peng, Dezhong and Lv, Jiancheng and Peng, Xi},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={23986--23995},
  year={2023}
}
```


















