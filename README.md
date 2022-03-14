# All-in-one

Code for the paper: All in One: Exploring Unified Video-Language Pre-training [Arxiv]()
---

![ppl](figures/main_ppl.png)

## Install

### 1.  PytorchLighting
In this work, we use PytorchLighting for distributed training.
Install pytorch and PytorchLighting first.

### 2. On-the-fly decode
To speed up the pre-training, we adopt on-the-fly decode for fast IO.
Install ffmpeg and pytorchvideo (for data augmentation) as below.


We list a shell script for reference.
```bash
conda create -n allinone python=3.7
source activate allinone
conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch
cd [Path_To_This_Code]
pip install -r requirements.txt
sudo conda install -y ffmpeg
pip install ffmpeg-python
pip install pytorchvideo
```

## Download Pretrained Weights
We provide three pretrained weights in google driver.

|  Model   | Pretrained Weight  | Trained Log | Hparams |
|  ----  | ----  | ---- | ---- |
| All-in-one-Ti  | [Google Driver](https://drive.google.com/file/d/1-mS9U1xRnvumaftjhxJsr_t4WjJ-gp7t/view?usp=sharing) | [Google Driver](https://drive.google.com/file/d/1wG-iHe89TWrgG9autheAOfl59a8_Wn7C/view?usp=sharing) | [Google Driver](https://drive.google.com/file/d/1anmiQVpjs1Mi6rdg-sLRtWzu31RU6rNw/view?usp=sharing)|
| All-in-one-S | [Google Driver](https://drive.google.com/file/d/1ntyEsFWLG8XQZ9oliYsrRZmhp_OMbQJ-/view?usp=sharing) | [Google Driver](https://drive.google.com/file/d/1NAHFZSAhGWF_CY4MlE6mKoBIyb4gbOqp/view?usp=sharing) |  [Google Driver](https://drive.google.com/file/d/1Y6OAnBPuei6QcQSyIXuL08Zb7TWxR6ue/view?usp=sharing)|
| All-in-one-B | [Google Driver](https://drive.google.com/file/d/1z3g891ND6CGCUkVzCXr2647wVG-15uUS/view?usp=sharing) | [Google Driver](https://drive.google.com/file/d/1gaBEo91jo4ushI63uHBltrbSXJRLPd_K/view?usp=sharing) | [Google Driver](https://drive.google.com/file/d/16J0zsJUt4yUfOc93k4xX8Z9FW-7M_Bdl/view?usp=sharing) |

After downloaded these pretrained weights, move them into pretrained dir.
```bash
mkdir pretrained
cp *.ckpt pretrained/
```


## Dataset Preparation
See [`DATA.md`](DATA.md)

## Train New Models
See [`TRAIN.md`](TRAIN.md)

## Evaluation
See [`EVAL.md`](EVAL.md)


## News
### 2022.3.14 The first version of AllInOne is released. The data.md is in progress.


## Citation
If you find our work helps, please cite our paper.

```bash

```

## Acknowledgement
This work is mainly based on [ViLT](https://github.com/dandelin/ViLT).