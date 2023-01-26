# A-Standardized-Approach-for-Skin-Detection-Analysis-of-the-Literature-and-Case-Studies
A Standardized Approach for Skin Detection: Analysis of the Literature and Case-Studies

Deep Semantic Segmentation in Skin Detection

The link for downloading the code for the ensemble of DeepLabV3+: https://github.com/LorisNanni/An-empirical-study-on-ensemble-of-segmentation-approaches

the links for HardNet and PVT are: https://github.com/james128333/HarDNet-MSEG https://github.com/DengPingFan/Polyp-PVT

the link for HSN is https://github.com/baiboat/HSNet

! very important, you should comment the line (in PVT, HSN and HardNet):

 res = (res - res.min()) / (res.max() - res.min() + 1e-8)
 
 otherwise you will always find a foreground region
 
 see line 40 of https://github.com/james128333/HarDNet-MSEG/blob/master/Test.py
 
 see line 40 of https://github.com/DengPingFan/Polyp-PVT/blob/main/Test.py
 
 see line 40 of https://github.com/baiboat/HSNet/blob/main/Test.py
 
 
 
 you could comment that normalization also in the training set, e.g. if you use images without foreground pixels.
 
