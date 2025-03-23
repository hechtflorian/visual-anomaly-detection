# Visual Anomaly Detection Benchmark with Industrial Images

This is a simple industrial benchmark used to study unsupervised anomaly detection models using Anomalib.
The model performance is evaluated in terms of accuracy and efficiency, focusing on the classification task.
To measure the model accuracy, the following Metrics are used: AU-ROC, AU-PR, F1Score.
For the model efficiency, the latency and the throughput is measured.
To obtain and check the results for each model and image-size, all the models can be tested seperately.

## Supported Models
- EfficientAD (S and M variants)
- FastFlow
- PatchCore (10% and 1% variants)

## Supported Datasets
- MVTec AD (automatically downloaded if not present. You can also find the dataset at: https://www.mvtec.com/company/research/datasets/mvtec-ad)
- Rubber Mats (needs manual download. You can contact Data Spree GmbH to get access to the dataset: https://www.data-spree.com/de/kontakt)
- MVTec Multiclass (needs to be downloaded and set up)

## Requirements
- Python 3.8+
- PyTorch 2.0.0+
- Anomalib 1.2.0
- Other dependencies listed in requirements.txt

## Usage
1. Install requirements: `pip install -r requirements.txt`
2. Open the notebook `anomalib_benchmark.ipynb`
3. Modify the configuration parameters at the top
4. Run the cells to get the Results

## References
- Anomalib library von Samet et al. (2022), https://github.com/openvinotoolkit/anomalib
- MVTec AD von Bergman et al. (2021)
- Rubber Mats Dataset von Data Spree GmbH: https://www.data-spree.com/de

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
