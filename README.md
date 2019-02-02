# BERT-Classification-Tutorial
Labeling data can be said to be the most difficult task in AI model training. The data annotation of natural language processing requires a lot of manpower. Compared with computer vision image annotation, text annotation usually does not have accurate standard answers. The understanding of sentences varies from person to person, making this work even more difficult. but! Google recently released the BERT to solve this problem! According to our experiments, BERT can bring significant classification accuracy improvement under extremely small data in the task of text multi-classification. Moreover, the main comparison of the experiment is the state of the art language model migration learning model released only 5 months ago - ULMFiT (https://arxiv.org/abs/1801.06146), the results have a significant improvement.
![alt text](https://github.com/Socialbird-AILab/BERT-Classification-Tutorial/blob/master/pictures/Results.png)

As can be seen from the above figure, BERT has excellent performance in different data sets. The experimental data we used was divided into 1000, 6700 and 12000, and each contained test data, and the training test was divided into 80%-20%. Datasets are obtained from multiple web sources and have undergone a series of classification mappings. However, the Noisy data set has a relatively significant noise, and the sampling statistics show that the noise ratio is around 20%. The experiment compared several models, from the most basic convolutional network as Baseline, to the convolutional network plus the traditional word vector Glove embedding, then ULMFiT and BERT.

# 1. Operating environment
The Tensorflow version is Windows 1.10.0 GPU. The specific installation tutorial can refer to this link https://www.tensorflow.org/install/pip?lang=python3. The Anaconda version is 1.9.2.

# 2. Hardware configuration
The experimental machine graphics card is NVIDIA GeForce GTX 1080 Ti, and the BERT base model occupies approximately 9.5G of video memory.

# 3. Download the model
After all the operating environments are set up, you can download them to our experiment here. BERT base: https://storage.googleapis.com/bert_models/2018_10_18/uncased_L-12_H-768_A-12.zip
Once downloaded, place it in BERT_BASE_DIR.

# 4. Enter data preparation
We need to divide the text data into three parts:
" Train: train.tsv
" Evaluate: dev.tsv
" Test: test.tsv
The format of each file can be seen below. It is very simple. One column is the text data that needs to be classified, and the other column is the corresponding Label.

The data folder contains 1000 sample data of 10 categories and is divided into training and test sets.
![alt text](https://github.com/Socialbird-AILab/BERT-Classification-Tutorial/blob/master/pictures/Our%20data%20example.png)

# 5. Implementation details
Run run_classifier.py to implement text sorting tasks for 1000 10-category sample data. Please refer to the tutorial for details of the implementation: https://mp.weixin.qq.com/s/XmeDjHSFI0UsQmKeOgwnyA

