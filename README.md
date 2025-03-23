# Visual Anomaly Detection Benchmark with Industrial Images

This is a simple industrial benchmark for unsupervised anomaly detection models using Anomalib.
The model performance is evaluated in terms of accuracy and efficiency, focusing on the classification task.
To measure the model accuracy, the following Metrics are used: AU-ROC, AU-PR, F1Score.
For the model efficiency, the latency and the throughput is measured.
To obtain and check the results for each model and image-size, all the models can be tested seperately.

## Supported Models
- EfficientAD (S and M variants)
- FastFlow
- PatchCore (10% and 1% variants)

## Supported Datasets
- MVTec AD (automatically downloaded if not present)
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
