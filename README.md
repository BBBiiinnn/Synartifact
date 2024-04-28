# SynArtifact
This repository contains SynArtifact-1k proposed in [SynArtifact: Classifying and Alleviating Artifacts in Synthetic Images via Vision-Language Model](https://arxiv.org/abs/2402.18068).

## Instruction
We release SynArtifact-1k, the first synthetic image dataset can be utilized for artfiact classification and detection. SynArtifact-1k contains 1.3K synthetic images generated by various generative models. Each image is annotated rich information, such as artifact label, bounding box, caption. 
![](images/1.png)
Each synthetic image with artifacts is annotated with bounding box and caption. Then, annotator maps the artifact caption into artifact taxonomy.

## Data Structure
The entire data set is divided into 5 components. Each split of dataset consists of three parts: `annotation_image`, which contains synthetic images with annotation, `annotation_json_artifacts_class`, which provides artifact label, bounding box and caption of synthetic images, images, which contains originally synthetic images. `train.txt` and `eval.txt` contain image path of training set and evaluation set respectively. `artifact_class.csv` contains the index of the artifact label.
```
data
├── sub_data_0                      
│   ├── annotation_image
│   │   ├── <annotated_image #1  >
│   │   ├── <annotated_image #2  >
│   │   └── <annotated_image #...>
│   │
│   ├── annotation_json_artifacts_class
│   │   ├── <annotated_json #1  >
│   │   ├── <annotated_json #2  >
│   │   └── <annotated_json #...>
│   │
│   ├── images
│   │   ├── <synthetic image #1  >
│   │   ├── <synthetic image #2  >
│   │   └── <synthetic image #...>
│
├── sub_data_1                   
│   ├── annotation_image
│   ├── annotation_json_artifacts_class
│   └── images
│
├── sub_data_2                   
│   ├── annotation_image
│   ├── annotation_json_artifacts_class
│   └── images
│
├── sub_data_3                    
│   ├── annotation_image
│   ├── annotation_json_artifacts_class
│   └── images
│
├── sub_data_4                   
│   ├── annotation_image
│   ├── annotation_json_artifacts_class
│   └── images
|
├── artifact_class.csv
|
├── train.txt
└── eval.txt                      
```

## Citation
```
@article{cao2024synartifact,
  title={SynArtifact: Classifying and Alleviating Artifacts in Synthetic Images via Vision-Language Model},
  author={Cao, Bin and Yuan, Jianhao and Liu, Yexin and Li, Jian and Sun, Shuyang and Liu, Jing and Zhao, Bo},
  journal={arXiv preprint arXiv:2402.18068},
  year={2024}
}
```
