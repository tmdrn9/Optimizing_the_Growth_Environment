# Optimizing_the_Growth_Environment
[Dacon/KIST 강릉분원/생육 환경 최적화 경진대회](https://dacon.io/competitions/official/235897/overview/description)

Team 'remember' : 이승리, 서원진, 최재홍, 최민기

Private 27th, Score 0.16078 (27/136, 19.8%)

----

### Development Environment

- Google Colab pro

### Train 

- data split : 0.8/0.2 (train/validation)
- nomalization : mean=(0.7565022, 0.77448946, 0.81488067), std=(0.17942707, 0.16611606, 0.1944418)
- loss : L1Loss
- optimizer : AdamW
- scheduler : CosineAnnealingWarmRestarts

- model1 : mixmet_l
  - input size : 224
  - augmentation : HorizontalFlip, VeriticalFlip, Rotate
  - epoch : 100
  - batch size : 64
  - lr :  0.0001
 
- model2 : swin_base_patch4_window12_384_in22k
  - input size : 384
  - augmentation : HorizontalFlip, RandomBrightnessContrast, Cutout, HueSaturationValue, ColorJitter
  - epoch : 300
  - batch size : 16
  - lr : 0.0002


### Inference 

- Ensemble(soft-voting)

---
