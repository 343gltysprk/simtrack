## Exploring Simple 3D Multi-Object Tracking for Autonomous Driving
<p align='left'>
  <img src='example.gif' width='721'/>
</p>

[Chenxu Luo](https://chenxuluo.github.io/), [Xiaodong Yang](https://xiaodongyang.org/), [Alan Yuille](https://www.cs.jhu.edu/~ayuille/) <br>
Exploring Simple 3D Multi-Object Tracking for Autonomous Driving, ICCV 2021<br>
[[Paper]](https://arxiv.org/pdf/2108.10312.pdf) [[Poster]](poster.pdf) [[YouTube]](https://www.youtube.com/watch?v=awK1O-wf_74)

## Getting Started
### Installation
Please refer to [INSTALL](INSTALL.md) for the detail.

### Data Preparation 
* Down load [nuScenes mini]([https://www.nuscenes.org](https://www.nuscenes.org/nuscenes#download))
```
python ./tools/create_data.py nuscenes_data_prep --root_path=NUSCENES_TRAINVAL_DATASET_ROOT --version="v1.0-mini" --nsweeps=10
```

Soft link the dataset to this directory.

### Run

```
python ./tools/val_nusc_tracking.py examples/point_pillars/configs/nusc_all_pp_centernet_tracking.py --checkpoint model_zoo/simtrack_pillar.pth --work_dir experiments
```

If you encounter problems during evaluation, try upgrading nuscenes-devkit.

## Citation
Please cite the following paper if this repo helps your research:
```bibtex
@InProceedings{Luo_2021_ICCV,
    author    = {Luo, Chenxu and Yang, Xiaodong and Yuille, Alan},
    title     = {Exploring Simple 3D Multi-Object Tracking for Autonomous Driving},
    booktitle = {International Conference on Computer Vision (ICCV)},
    year      = {2021}
}
```

## License
Copyright (C) 2021 QCraft. All rights reserved. Licensed under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) (Attribution-NonCommercial-ShareAlike 4.0 International). The code is released for academic research use only. For commercial use, please contact [business@qcraft.ai](business@qcraft.ai).
