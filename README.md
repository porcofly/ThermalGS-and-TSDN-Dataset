
# ThermalGS: Dynamic Thermal 3D Reconstruction with 3D Gaussian Splatting


## Overview
This repository contains the official implementation of **ThermalGS**, a novel dynamic thermal 3D reconstruction method based on 3D Gaussian Splatting, along with the **Thermal Scene Day-Night (TSDN)** dataset. Our method enables simultaneous reconstruction of scene geometry and dynamic thermal radiation characteristics using RGB and thermal infrared (TIR) images.

Key features:
- First framework for spatio-temporal thermal 3D reconstruction
- Achieves state-of-the-art performance with 1°C average absolute temperature error
- Enables prediction of surface temperature variations over time

## TSDN Dataset Structure 
The Thermal Scene Day-Night dataset is organized as follows:

```
data/
├─SingleTime_AM10/          # Morning capture (10:00 AM)
│  ├─raw_data/             # Raw sensor data
│  │  └─origin_images/     # Original RGB/TIR image pairs
│  ├─train/                # Training split
│  └─test/                 # Testing split
│
├─SingleTime_[XX]/         # Other capture times (AM00/PM14/PM18/PM22)
│
├─CrossTime/               # Cross-temporal sequences
│  ├─train/                # Mixed-time training data
│  └─test/                 # Mixed-time testing data
│
├─Temperature/             # Temperature prediction tasks
│  ├─CrossTime_4toPM14_Temp/  # 4PM→2PM prediction
│  ├─CrossTime_4toPM18_Temp/  # 4PM→6PM prediction
│  ├─CrossTime_4toPM22_Temp/  # 4PM→10PM prediction
│  └─CrossTime_Temp/          # General cross-time prediction
├─RGB_image
├─  ├─train
├─  ├─test
├─  └─val
├─mesh.mtl
├─mesh.obj
└─points3d.ply
```
​**Download TSDN dataset**:  [[OneDrive]](https://1drv.ms/u/s!AuxIu5p3iyOxiGeExKUHh35V4HWB?e=8UA0IM)
  
   

**Note**: You need to copy `mesh.mtl`, `mesh.obj`, `points3d.ply` to corresponding folders or modify path settings in the code to ensure proper data loading


## Getting Started

The complete code will be released as soon as possible.

## Citation
If you use our work in your research, please cite:
```bibtex
@article{thermalgs2025,
AUTHOR = {Liu, Yuxiang and Chen, Xi and Yan, Shen and Cui, Zeyu and Xiao, Huaxin and Liu, Yu and Zhang, Maojun},
TITLE = {ThermalGS: Dynamic 3D Thermal Reconstruction with Gaussian Splatting},
JOURNAL = {Remote Sensing},
VOLUME = {17},
YEAR = {2025},
NUMBER = {2},
ARTICLE-NUMBER = {335},
URL = {https://www.mdpi.com/2072-4292/17/2/335},
ISSN = {2072-4292},
DOI = {10.3390/rs17020335}
}
```

## License
This project is released under the [MIT License](LICENSE). The TSDN dataset is available for non-commercial research use only.


