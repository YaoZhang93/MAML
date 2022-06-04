# Modality-aware Mutual Learning for Multi-modal Medical Image Segmentation

## Paper

This is the implementation for the paper:

[Modality-aware Mutual Learning for Multi-modal Medical Image Segmentation](https://arxiv.org/pdf/2107.09842.pdf)

Early Accepted to MICCAI 2021

![image](https://github.com/YaoZhang93/MAML/blob/main/figs/MAML.png)

## Usage. 

* Data Preparation

  - Download the data from [MICCAI 2018 BraTS Challenge](https://www.med.upenn.edu/sbia/brats2018/data.html).

  - Convert the files' name by

  `python dataset_conversion/Task032_BraTS_2018.py`

  - Preprocess the data by

  `python experiment_planning/nnUNet_plan_and_preprocess.py -t 32 --verify_dataset_integrity`

* Train

  - Train the model by

  `python run/run_training.py 3d_fullres MAMLTrainerV2 32 0`

* Test

  - inference on the test data by

  `python inference/predict_simple.py -i INPUT_PATH -o OUTPUT_PATH -t 32 -f 0 -tr MAMLTrainerV2`

 `MAML` is integrated with the out-of-box [nnUNet](https://github.com/MIC-DKFZ/nnUNet). Please refer to it for more usage.

## Citation

If you find this code and paper useful for your research, please kindly cite our paper.

```
@inproceedings{zhang2021modality,
  title={Modality-Aware Mutual Learning for Multi-modal Medical Image Segmentation},
  author={Zhang, Yao and Yang, Jiawei and Tian, Jiang and Shi, Zhongchao and Zhong, Cheng and Zhang, Yang and He, Zhiqiang},
  booktitle={International Conference on Medical Image Computing and Computer-Assisted Intervention},
  pages={589--599},
  year={2021},
  organization={Springer}
}
```

## Acknowledgement

`MAML` is integrated with the out-of-box [nnUNet](https://github.com/MIC-DKFZ/nnUNet).
