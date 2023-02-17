<p align="right">English | <a href="">简体中文</a></p>

<p align="center">
  <img src="docs/figs/logo.png" align="center" width="21.5%">
  
  <h3 align="center"><strong>Robo3D: Towards Robust and Reliable 3D Perception against Common Corruptions</strong></h3>

  <p align="center">
  </p>

</p>

<p align="center">
  <a href="" target='_blank'>
    <img src="https://img.shields.io/badge/Paper-%F0%9F%93%83-slategray">
  </a>
  
  <a href="" target='_blank'>
    <img src="https://img.shields.io/badge/Project-%F0%9F%94%97-lightblue">
  </a>
  
  <a href="" target='_blank'>
    <img src="https://img.shields.io/badge/Demo-%F0%9F%8E%AC-pink">
  </a>
  
  <a href="" target='_blank'>
    <img src="https://img.shields.io/badge/%E4%B8%AD%E8%AF%91%E7%89%88-%F0%9F%90%BC-firebrick">
  </a>
</p>



## About
`Robo3D` is an evaluation benchmark heading toward robust and reliable 3D perception in autonomous driving. With it, we probe the robustness of 3D detectors and segmentors under out-of-distribution (OoD) scenarios against corruptions that tend to occur in the real-world environment. Specifically, we consider natural corruptions happen in the following cases:
1. **Adversarial weather conditions**, such as `fog`, `wet ground`, and `snow`;
2. **External disturbances** that are caused by `motion blur` or result in LiDAR `beam missing`;
3. **Internal sensor failure**, including LiDAR `crosstalk` and possible `incomplete echo`.

| | | | |
| :---: | :---: | :---: | :---: |
| <img src="docs/figs/clean.png" width="180" height="80"> | <img src="docs/figs/fog.png" width="180" height="80"> | <img src="docs/figs/wet_ground.png" width="180" height="80"> | <img src="docs/figs/snow.png" width="180" height="80"> |
| **Clean** | **Fog** | **Wet Ground** | **Snow** |
| <img src="docs/figs/motion_blur.png" width="180" height="80"> | <img src="docs/figs/beam_missing.png" width="180" height="80"> | <img src="docs/figs/crosstalk.png" width="180" height="80"> | <img src="docs/figs/incomplete_echo.png" width="180" height="80"> |
| **Motion Blur** | **Beam Missing** | **Crosstalk** | **Incomplete Echo** |
| | | | |

Visit our [project page]() to explore more examples. :red_car:



## Updates
- [2023.02] - The `KITTI-C`, `SemanticKITTI-C`, `nuScenes-C`, and `WaymoOpen-C` datasets are ready for downloading! See [here](docs/DATA_PREPARE.md) for more details.


## Outline
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Getting Started](#getting-started)
- [Taxonomy](#taxonomy)
- [Model Zoo](#model-zoo)
- [Benchmark](#benchmark)
- [Create Corruption Sets](#create-corruption-sets)
- [TODO List](#todo-list)
- [Citation](#citation)
- [License](#license)
- [Acknowledgements](#acknowledgements)


## Installation
For details related to installation, kindly refer to [INSTALL.md](docs/INSTALL.md).


## Data Preparation

Kindly refer to [DATA_PREPARE.md](docs/DATA_PREPARE.md) for the details to prepare the <sup>1</sup>`KITTI`, <sup>2</sup>`KITTI-C`, <sup>3</sup>`SemanticKITTI`, <sup>4</sup>`SemanticKITTI-C`, <sup>5</sup>`nuScenes`, <sup>6</sup>`nuScenes-C`, <sup>7</sup>`WaymoOpen`, and <sup>8</sup>`WaymoOpen-C` datasets.


## Getting Started

To learn more usage about this codebase, kindly refer to [GET_STARTED.md](docs/GET_STARTED.md).


## Taxonomy
To be updated.


## Model Zoo

<details open>
<summary>&nbsp<b>LiDAR Semantic Segmentation</b></summary>

> - [x] **[SqueezeSeg](https://arxiv.org/abs/1710.07368), ICRA 2018.** <sup>[**`[Code]`**](https://github.com/BichenWuUCB/SqueezeSeg)</sup>
> - [x] **[SqueezeSegV2](https://arxiv.org/abs/1809.08495), ICRA 2019.** <sup>[**`[Code]`**](https://github.com/xuanyuzhou98/SqueezeSegV2)</sup>
> - [x] **[MinkowskiNet](https://arxiv.org/abs/1904.08755), CVPR 2019.** <sup>[**`[Code]`**](https://github.com/NVIDIA/MinkowskiEngine)</sup>
> - [x] **[RangeNet++](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/milioto2019iros.pdf), IROS 2019.** <sup>[**`[Code]`**](https://github.com/PRBonn/lidar-bonnetal)</sup>
> - [x] **[KPConv](https://arxiv.org/abs/1904.08889), ICCV 2019.** <sup>[**`[Code]`**](https://github.com/HuguesTHOMAS/KPConv)</sup>
> - [x] **[SalsaNext](https://arxiv.org/abs/2003.03653), ISVC 2020.** <sup>[**`[Code]`**](https://github.com/TiagoCortinhal/SalsaNext)</sup>
> - [ ] **[RandLA-Net](https://arxiv.org/abs/1911.11236), CVPR 2020.** <sup>[**`[Code]`**](https://github.com/QingyongHu/RandLA-Net)</sup>
> - [x] **[PolarNet](https://arxiv.org/abs/2003.14032), CVPR 2020.** <sup>[**`[Code]`**](https://github.com/edwardzhou130/PolarSeg)</sup>
> - [ ] **[3D-MiniNet](https://arxiv.org/abs/2002.10893), IROS 2020.** <sup>[**`[Code]`**](https://github.com/Shathe/3D-MiniNet)</sup>
> - [x] **[SPVCNN](https://arxiv.org/abs/2007.16100), ECCV 2020.** <sup>[**`[Code]`**](https://github.com/mit-han-lab/spvnas)</sup>
> - [x] **[Cylinder3D](https://arxiv.org/abs/2011.10033), CVPR 2021.** <sup>[**`[Code]`**](https://github.com/xinge008/Cylinder3D)</sup>
> - [x] **[FIDNet](https://arxiv.org/abs/2109.03787), IROS 2021.** <sup>[**`[Code]`**](https://github.com/placeforyiming/IROS21-FIDNet-SemanticKITTI)</sup>
> - [x] **[RPVNet](https://arxiv.org/abs/2103.12978), ICCV 2021.**
> - [x] **[CENet](https://arxiv.org/abs/2207.12691), ICME 2022.** <sup>[**`[Code]`**](https://github.com/huixiancheng/CENet)</sup>
> - [ ] **[CPGNet](https://arxiv.org/abs/2204.09914), ICRA 2022.** <sup>[**`[Code]`**](https://github.com/GangZhang842/CPGNet)</sup>
> - [x] **[2DPASS](https://arxiv.org/abs/2207.04397), ECCV 2022.** <sup>[**`[Code]`**](https://github.com/yanx27/2DPASS)</sup>
> - [x] **[GFNet](https://arxiv.org/abs/2207.02605), TMLR 2022.** <sup>[**`[Code]`**](https://github.com/haibo-qiu/GFNet)</sup>
> - [ ] **[PCB-RandNet](https://arxiv.org/abs/2209.13797), arXiv 2022.** <sup>[**`[Code]`**](https://github.com/huixiancheng/PCB-RandNet)</sup>
> - [ ] **[PIDS](https://arxiv.org/abs/2211.15759), WACV 2023.** <sup>[**`[Code]`**](https://github.com/lordzth666/WACV23_PIDS-Joint-Point-Interaction-Dimension-Search-for-3D-Point-Cloud)</sup>
> - [x] **[WaffleIron](http://arxiv.org/abs/2301.10100), arXiv 2023.** <sup>[**`[Code]`**](https://github.com/valeoai/WaffleIron)</sup>

</details>


<details open>
<summary>&nbsp<b>3D Object Detection</b></summary>

> - [x] **[SECOND](https://www.mdpi.com/1424-8220/18/10/3337), Sensors 2018.** <sup>[**`[Code]`**](https://github.com/traveller59/second.pytorch)</sup>
> - [x] **[PointPillars](https://arxiv.org/abs/1812.05784), CVPR 2019.** <sup>[**`[Code]`**](https://github.com/nutonomy/second.pytorch)</sup>
> - [x] **[PointRCNN](https://arxiv.org/abs/1812.04244), CVPR 2019.** <sup>[**`[Code]`**](https://github.com/sshaoshuai/PointRCNN)</sup>
> - [x] **[Part-A2](https://arxiv.org/abs/1907.03670), TPAMI 2020.**
> - [x] **[PV-RCNN](https://arxiv.org/abs/1912.13192), CVPR 2020.** <sup>[**`[Code]`**](https://github.com/sshaoshuai/PV-RCNN)</sup>
> - [x] **[CenterPoint](https://arxiv.org/abs/2006.11275), CVPR 2021.** <sup>[**`[Code]`**](https://github.com/tianweiy/CenterPoint)</sup>

</details>


## Benchmark

### LiDAR Semantic Segmentation

#### SemanticKITTI-C
| Model | $\text{mCE}$ | $\text{mRR}$ | Clean | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Cross-Talk | Incomplete Echo |
| :---------------: | :--: | :--: | :-----: | :-----: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
| [SqueezeSeg](docs/results/SqueezeSeg.md) |  | $72.81$ | $31.61$ | $18.85$ | $27.30$ | $22.70$ | $17.93$ | $25.01$ | $21.65$ | $27.66$ |
| [SqueezeSegV2](docs/results/SqueezeSegV2.md) |  | $70.54$ | $41.28$ | $25.64$ | $35.02$ | $27.75$ | $22.75$ | $32.19$ | $26.68$ | $33.80$ |
| [RangeNet-dark21](docs/results/RangeNet-dark21.md) |  |  | $47.15$ | $31.04$ | $42.23$ | $37.43$ | $37.79$ | $38.16$ | $40.65$ | $43.06$ |
| [RangeNet-dark53](docs/results/RangeNet-dark21.md) |  |  | $50.29$ | $36.33$ | $45.22$ | $40.02$ | $38.07$ | $40.80$ | $47.42$ | $44.31$ |
| SalsaNext         |  |  | $55.80$ | $34.89$ | $50.78$ | $45.55$ | $53.16$ | $49.63$ | $45.40$ | $52.65$ |
| FIDNet            |      |      |         |         |         |         |         |         |         |         |
| CENet             |  |  | $62.55$ | $42.70$ | $58.62$ | $53.64$ | $59.26$ | $55.78$ | $50.99$ | $58.41$ |
|                   |      |      |         |         |         |         |         |         |         |         |
| KPConv            | $$ | $$ | $62.17$ | $54.46$ | $59.23$ | $54.15$ | $48.09$ | $57.35$ | $58.80$ | $58.52$ |
| WaffleIron        | $$ | $$ | $66.04$ | $45.52$ | $63.33$ | $49.30$ | $42.49$ | $59.28$ | $30.79$ | $63.06$ |
|                   |      |      |         |         |         |         |         |         |         |         |
| PolarNet          | $$ | $$ | $58.17$ | $38.74$ | $53.11$ | $49.42$ | $53.18$ | $54.10$ | $33.30$ | $52.30$ |
|                   |      |      |         |         |         |         |         |         |         |         |
| MinkUNet-18_cr1.0 | $$ | $$ | $62.76$ | $55.87$ | $59.06$ | $53.28$ | $53.93$ | $56.32$ | $60.46$ | $58.68$ |
| MinkUNet-34_cr1.6 | $$ | $$ | $63.78$ | $53.54$ | $60.12$ | $50.17$ | $55.82$ | $57.35$ | $61.22$ | $58.92$ |
| Cylinder3D        |      |      |         |         |         |         |         |         |         |         |
| Cylinder3D-TS     | $$ | $$ | $61.00$ | $37.11$ | $56.63$ | $45.39$ | $60.22$ | $56.81$ | $57.10$ | $58.34$ |
|                   |      |      |         |         |         |         |      |  |         |         |         |
| SPVCNN-18_cr1.0   | $$ | $$ | $62.47$ | $55.32$ | $58.87$ | $51.42$ | $54.09$ | $56.67$ | $60.18$ | $58.55$ |
| SPVCNN-34_cr1.6   | $$ | $$ | $63.22$ | $56.53$ | $59.67$ | $52.35$ | $55.99$ | $56.76$ | $61.22$ | $59.05$ |
| RPVNet            | $$ | $$ | $63.75$ | $47.64$ | $55.71$ | $51.13$ | $59.29$ | $53.51$ | $30.63$ | $59.59$ |
| 2DPASS            | $$ | $$ | $64.61$ | $40.46$ | $61.55$ | $48.53$ | $62.99$ | $58.78$ | $36.10$ | $60.45$ |
| GFNet             | $$ | $$ | $63.00$ | $42.04$ | $58.87$ | $56.71$ | $61.29$ | $56.95$ | $29.53$ | $59.27$ |


#### nuScenes-C
| Model             | mCE | mRR | Clean  | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Crosstalk | Incomplete Echo |
| :---------------: | :-----: | :-----: |:-----: | :-------: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
|                   |         |         |  |    |      |       |      |  |     | |


#### WaymoOpen-C
| Model             | mCE | mRR | Clean  | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Crosstalk | Incomplete Echo |
| :---------------: | :-----: | :-----: |:-----: | :-------: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
|                   |         |         |  |    |      |       |      |  |     | |


### 3D Object Detection

#### KITTI-C
| Model             | mCE | mRR | Clean  | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Crosstalk | Incomplete Echo |
| :---------------: | :-----: | :-----: |:-----: | :-------: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
|                   |         |         |  |    |      |       |      |  |     | |


#### nuScenes-C
| Model             | mCE | mRR | Clean  | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Crosstalk | Incomplete Echo |
| :---------------: | :-----: | :-----: |:-----: | :-------: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
|                   |         |         |  |    |      |       |      |  |     | |


#### WaymoOpen-C
| Model             | mCE | mRR | Clean  | Fog | Wet Ground | Snow | Motion Blur | Beam Missing | Crosstalk | Incomplete Echo |
| :---------------: | :-----: | :-----: |:-----: | :-------: | :--------: | :---------: | :---------: | :----: | :-------: | :----: |
|                   |         |         |  |    |      |       |      |  |     | |



## Create Corruption Sets
You can manage to create your own "RoboDet" corrpution sets! Follow the instructions listed in [CREATE.md](docs/CREATE.md).


## TODO List
- [x] Initial release. 🚀
- [x] Add scripts for creating common corruptions.
- [ ] Add download links for corruption sets.
- [ ] Add evaluation scripts on corruption sets.
- [ ] ...


## Citation
If you find this work helpful, please kindly consider citing our paper:

```bibtex
@ARTICLE{robo3d,
  title={Robo3D: Towards Robust and Reliable 3D Perception against Common Corruptions},
  author={xxx},
  journal={arXiv preprint arXiv:23xx.xxxxx}, 
  year={2023},
}
```


## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a>
<br />
This work is under the <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>, while some specific operations in this codebase might be with other licenses. Please refer to [LICENSE.md](docs/LICENSE.md) for a more careful check, if you are using our code for commercial matters.


## Acknowledgements
We thank the exceptional support from [Shanghai AI Laboratory](https://www.shlab.org.cn/)! Kindly refer to [ACKNOWLEDGE.md](docs/ACKNOWLEDGE.md) for more detailed acknowledgments of this codebase.

<img src="docs/figs/shlab.png" align="center" width="96%">



