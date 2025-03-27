# Anomaly Detection Benchmark with Industrial Images

This is a simple industrial benchmark to study unsupervised anomaly detection models using Anomalib.
The model performance is evaluated in terms of accuracy and efficiency, focusing on the classification task.
To measure the model accuracy, the following Metrics are used: AU-ROC, AU-PR, F1Score.
For the model efficiency, the latency and the throughput is measured.
All the models can be tested seperately on the datasets to evaluate their performance.

## Models
- EfficientAD (S and M variants)
- PatchCore (10% and 1% variants)
- FastFlow

## Datasets
- MVTec AD (automatically downloaded if not present. You can also find the dataset at: https://www.mvtec.com/company/research/datasets/mvtec-ad)
- Rubber Mats (needs manual download. You can contact Data Spree GmbH to get your access to the dataset: https://www.data-spree.com/de/kontakt)
- MVTec AD Multiclass (MVTec AD will be downloaded automatically if not present, while the multi-class folders need setup)

## Requirements
- Python 3.8+
- PyTorch 2.0.0+
- Anomalib 1.2.0
- Other dependencies listed in requirements.txt

## Usage
1. Install requirements: `pip install -r requirements.txt`
2. Open the notebook `anomalib_benchmark.ipynb`
3. Modify the configuration parameters at the top
4. Run the cells to get the results

You can also simply run the notebook in google colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hechtflorian/visual-anomaly-detection/blob/main/anomalib-benchmark.ipynb)

Benchmark-Configuration:
- First, please check if the requirements are installed correctly. If you are having trouble, please make sure to run the problem fixes in the installation part at the top.
- Then, choose the benchmark dataset. For MVTec AD, you should also configure the category.
- Select model and image-size.
- Optionally provide your dataset root. If you do not have the MVTec AD dataset, it will be downloaded automatically.
- Also, you can optionally connect Comet Logger for Experiment management.
- Now you can run the Benchmark. Please use the GPU for optimal results!

Note: For the efficiency measurement, 100 runs are configured for demo cases. To get proper results, 1000 runs should be configured instead.

## References
- Anomalib library, vgl. Samet et al. (2022): https://github.com/openvinotoolkit/anomalib
- MVTec AD, vgl. Bergmann et al. (2021): https://www.mvtec.com/company/research/datasets/mvtec-ad
- Rubber Mats Dataset (© 2024 Data Spree GmbH): https://www.data-spree.com/de

Please contact Data Spree to get your access to the Rubber Mats Dataset: https://www.data-spree.com/de/kontakt


Akcay, Samet, Dick Ameln, Ashwin Vaidya, Barath Lakshmanan, Nilesh Ahuja und Utku
Genc (2022). „Anomalib: A Deep Learning Library for Anomaly Detection“. In: 2022
IEEE International Conference on Image Processing (ICIP). IEEE, S. 1706–1710. isbn:
978-1-6654-9620-9.  doi: 10.1109/ICIP46576.2022.9897283

Bergmann, Paul, Kilian Batzner, Michael Fauser, David Sattlegger und Carsten Steger
(2021). „The MVTec Anomaly Detection Dataset: A Comprehensive Real-World Dataset
for Unsupervised Anomaly Detection“. In: International Journal of Computer Vision
129.4, S. 1038–1059. issn: 0920-5691. doi: 10.1007/s11263-020-01400-4

BibTeX:
```bibtex
@inproceedings{akcay2022anomalib,
  title={Anomalib: A deep learning library for anomaly detection},
  author={Akcay, Samet and Ameln, Dick and Vaidya, Ashwin and Lakshmanan, Barath and Ahuja, Nilesh and Genc, Utku},
  booktitle={2022 IEEE International Conference on Image Processing (ICIP)},
  pages={1706--1710},
  year={2022},
  organization={IEEE}
}

@article{Bergmann.2021,
 author = {Bergmann, Paul and Batzner, Kilian and Fauser, Michael and Sattlegger, David and Steger, Carsten},
 year = {2021},
 title = {The MVTec Anomaly Detection Dataset: A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection},
 pages = {1038--1059},
 volume = {129},
 number = {4},
 issn = {0920-5691},
 journal = {International Journal of Computer Vision},
 doi = {10.1007/s11263-020-01400-4 }
}
