# Deep Learning based road extraction from historical maps 
This repository contains the code, test patches and weights for the paper [Deep Learning based road extraction from historical maps]

# Dataset (Source)
---------------------
[Turkey 1:200k Historical Topographic Maps](https://urbanoccupations.ku.edu.tr/historical-road-types-for-turkey-1940s/)

The historical DHK 200 Turkey map used in this study covers a large area of around
150,000 square km in northwest Turkey, including the regions of Ankara and Bursa.
The DHK 200 Turkey map legends are organized bilingually in accordance with the rest of the World War II German military
maps [1].

| Model              | Batch-Size | F-1 Score | Weights | No. Of Params | 
|:--------------------------:|:------------------:|-------------------------:|-------------------------:|
|Timm-resnest200e(U-Net++)   | 16 Batch-Size      | **0,577**   |      68M      | [Timm-resnest200e.pth](https://drive.google.com/drive/folders/146HRDz-075PTf-pyUQO-1ZrU4X1UQ5L2)                                 
|Timm-resnest200e(MA-Net)                         | 16 Batch-Size                 | 0,525      |       68M          | [MA-Net timm-resnest200e.pth](https://drive.google.com/drive/folders/146HRDz-075PTf-pyUQO-1ZrU4X1UQ5L2) 
|Inceptionv4(U-Net++)                          | 16 Batch-Size                 | 0,525         |      54M        | [Inceptionv4.pth](https://drive.google.com/drive/folders/146HRDz-075PTf-pyUQO-1ZrU4X1UQ5L2)                
|Densenet201(U-Net++)                          | 16 Batch-Size                 | 0,511       |      18M         | [Densenet201.pth](https://drive.google.com/drive/folders/146HRDz-075PTf-pyUQO-1ZrU4X1UQ5L2)
|Resnext50_32x4d(U-Net++)                          | 16 Batch-Size                | 0,491      |      42M          | [Resnext50_32x4d.pth](https://drive.google.com/drive/u/0/folders/1zQfCouyg3uVd76KNzYpbvrFJ4DGfUPdp)

# Framework
---------------------
![alt text](figures/framework.png)


# Models Comparison
---------------------
![alt text](figures/comparison.png)

Outputs
---------------------
![alt text](figures/resnest200e.png)




Prequsities
---------------------

The code was implemented in Python(3.8) and PyTroch(1.14.0) on Windows OS. The *Qubvel segmentation models pytorch* library is used as a baseline for implementation. 
Apart from main data science libraries, RS-specific libraries such as GDAL, rasterio, and tifffile are also required.

Citation
---------------------

[1] Ekim, B., Sertel, E., & Kabadayı, M. E. (2021). Automatic Road Extraction from Historical Maps Using Deep Learning Techniques: A Regional Case Study of Turkey in a German World War II Map. ISPRS International Journal of Geo-Information, 10(8), 492.

[2]qubvel/segmentation_models.pytorch: Segmentation models with pretrained backbones. PyTorch

Contact Information:
--------------------
Cengiz Avcı - avcice16@itu.edu.tr 
