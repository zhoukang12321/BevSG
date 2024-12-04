# Learning Bird’s Eye View Scene Graph and Knowledge-Inspired Policy for Embodied Visual Navigation


We propose BevNav framework to solve these issues by three parts: (i) we introduce a novel Bird’s Eye View (BEV) scene graph (BevSG) that utilizes multi-view 2D information transformed into 3D under the supervision of 3D detection to encode scene layouts and geometric clues. It can distinguish multi-view
semantically similar objects and make plans in this graph. (ii) we propose BEV-BLIP contrastive learning that aligns the BEV and language grounding inputs transferring constrain commonsense knowledge in pre-trained models without other training in the environments. (iii) we design BEV-based view search navigation policy, which encourages representations that encode the semantics, relationships, and positional information of objects. 

## Setup
- *Dependeces*: We use earlier (`0.2.2`) versions of [habitat-sim](https://github.com/facebookresearch/habitat-sim/tree/v0.2.2) and [habitat-lab](https://github.com/facebookresearch/habitat-lab/tree/v0.2.2). Other related depencese can be found in `requirements.txt`. 

- *Data (MatterPort3D)*: Please download the scene dataset and the episode dataset from [habitat-lab/DATASETS.md](https://github.com/facebookresearch/habitat-sim/blob/main/DATASETS.md#matterport3d-mp3d-dataset). Then organize the files as follows:
```
3dNav/
  data/
    scene_datasets/
        mp3d/
    episode_datasets/
        objectnav_mp3d_v1/
```

## Getting Started
For environment setup and dataset preparation, please follow:
* [Installation](./docs/installation.md)

For evaluation, please follow:
* [Evaluation](./docs/run.md)

## Training and Evaluating:

We provide scripts for quick training and evaluation. The parameters can be found in [sh_train_mp3d.sh](sh_train_mp3d.sh) and [sh_eval.sh](sh_eval.sh), You can modify these parameters to customize them according to your specific requirements.
```
sh sh_train_mp3d.sh # training 
sh sh_eval.sh # evaluating
```


