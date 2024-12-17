# Relaxed Rotational Equivariance via $G$-Biases in Vision
The AAAI2025 accepted this paper! We will release the code in the next few days.
### Ablation Experiments on the CIFAR-100 dataset
Unlike the ablation experiment reported in the paper, we simplified the classification header and re-conducted the ablation experiment, resulting in more prominent results. The results are as follows:
|Model Name|Group G|Type of Equivariance|Top-1 Acc.|#Param.|
|-|-|-|-|-|
|c2_sre_n|$C_2$|SRE|76.95|325748|
|c2_rre_n|$C_2$|RRE|77.84|345140|
|c4_sre_n|$C_4$|SRE|80.79|625012|
|c4_rre_n|$C_4$|RRE|82.48|663796|
|c6_sre_n|$C_6$|SRE|81.36|924276|
|c6_rre_n|$C_6$|RRE|83.20|982452|
|c8_sre_n|$C_8$|SRE|82.52|1223540|
|c8_rre_n|$C_8$|RRE|83.63|1301108|

You can train the model using the following command:

```
python classification/train.py -model [Model Name] -dataset [Dataset] -batch_size 128
```

**[Model Name]**: c2_sre_n, c2_rre_n, c4_sre_n, c4_rre_n, c6_sre_n, c6_rre_n, c8_sre_n, c8_rre_n

**[Dataset]**: cifar10, cifar100

Example command: 

```
python classification/train.py -model c4_rre_n -dataset cifar100 -batch_size 128
```

