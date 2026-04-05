# *Tea Leave Classification Using Machine Learning Approaches*
Tool Used: Python ([Google Collab](https://colab.research.google.com/drive/1Esfj_Ye5NSQTp6VBU3D0H4ACgiFJ4XIn?usp=sharing))

Data Source and its Citation: Alam, B M Shahria; Ahammed, Fahad; Kibria, Golam; Noor, Mohammad Tahmid; Shikdar, Omar Faruq; Mahazabin, Kazi Isat; Ali, Md Nawab Yousuf (2025), “teaLeafBD”, Mendeley Data, V3, doi: [10.17632/744vznw5k2.3](https://data.mendeley.com/datasets/744vznw5k2/3)

## Project Summary
### Problem
<p align='justify'>
Tea is the world’s most popular beverage, yet production is constantly threatened by disease. Traditional manual inspection is labor-intensive and prone to error. While Deep Learning (DL) were introduced to the solution, many models remain "black boxes," making it difficult for farmers to trust and adopt the technology.
</p>

### Solution
<p align='justify'>
The research addresses both accuracy and interpretability. By utilizing the teaLeafBD dataset, I conducted a comparative analysis between traditional standalone Convolutional Neural Networks(CNNs) and hybrid architectures (CNN-Machine Learning(ML)). To ensure the models are trustworthy, I integrated Grad-CAM visualization to produce heatmaps that highlight exactly which leaf features the model is focusing on.
</p>

## Project Objectives
1.	To implement standalone CNN models and hybrid CNN-ML models on the images of tea leaves.
2.	To interpret the results from CNN models on tea leaves disease classification by using Gradient-weighted Class Activation Mapping (Grad-CAM).
3.	To compare the performance of CNN models and hybrid CNN-ML models on tea leaves disease classification using performance metrics.

## Research Framework and Methodology
<p align='justify'>
The methodology for this study is structured into three distinct phases  (<b><i>data acquisition and data preparation, data modelling, and model interpretation and evaluation</i></b>), consisting of five core processes (<b><i>data collection, image preprocessing, model training among different pretrained CNN models and hybrid CNN-ML models, Grad-Cam visual interpretation, and model evaluation using performance metrices</i></b>) designed to optimize classification accuracy and model interpretability.
</p>

### Phase 1: Data Acquisition & Preparation
This phase focuses on building a robust foundation for the deep learning models.

* **Data collection**: Sourced the *teaLeafBD* dataset from Mendeley Data, consisting of six distinct tea leaf disease categories.
    * **Setting up binary scenario**: Combined all six distinct tea leaf disease categories into a single category "disease".
    * **Setting up multiclass scenario**: the same state of *teaLeafBD* dataset.
    * **Stratified Splitting**: Images were partitioned into **Training** (*70%*), **Validation** (*20%*), and **Testing** (*10%*) sets to ensure class balance across all subsets.
* **Image Preprocessing**: The images from **training set and validation set** undergone a series of image preprocessing to improve feature extraction efficiency during process of filtering under convolutional and pooling layers which are available in every pretrained CNN model, and to ensure consistency while reducing noise among the images. 
    * **Image Augmentation**: Applied to images from the **training set** during image preprocessing process. Notably, a subset of the ***original images without any augmentation applied was preserved*** for the model evaluation process to determine the performance improvement given by the process of image augmentation.

### Phase 2: Data Modelling
In this phase, two distinct architectural approaches were tested and optimized each in both binary and multiclass experimental scenario.

* **Standalone CNNs**: Pre-trained CNN (*VGG-16, MobileNetV2, EfficientNet_B1 and ResNet-50*) were trained and validated using the pre-processed validation set to prevent overfitting.

* **Hybrid CNN-ML Models**: Combined CNN feature extractors with ML classifiers (*SVM, RF and XGBoost*). These models underwent Hyperparameter Tuning via Randomized Search to ensure optimal performance.
  
### Phase 3: Model Evaluation and Interpretation

* **Grad-CAM**: Applied to standalone CNNs to generate heatmaps, providing a visual audit of the model's decision-making process.
* **Performance Metric**: Models were evaluated in both Binary and Multiclass scenarios using confusion matrix and performance metrics (*Accuracy, Recall, Precision and F1-score*).

Here is the research framework diagram:
<p align="center">
  <img src="media/1.png" width="900" title="Research Framework">
  <br>
</p>

## Results and Discussion
The results are break into two different experiment scenario (**binary and multiclass**). A total of 32 distinct model configurations were utilised in binary and multiclass experiment scenario.

The models were built by combining three key components:
1. **4 CNN Pre-trained Feature Extractors**: *VGG-16, MobileNetV2, EfficientNet_B1 and ResNet-50*

2. **4 Decision-Making Algorithms**: Standard CNN classifier (*SoftMax*)  and three ML Classifiers (*SVM, RF and XGBoost*)

3. **2 Training Regimes**: Models were trained on both Original Images and Augmented Images to quantify the impact of data augmentation on performance.

### Grad-Cam Visual (Binary)

#### Disease
Original:
<p align="center">
  <img src="media/2.png" width="250" title="O.D.B">
  <br>
</p>

Results:
<p align="center">
  <img src="media/3.png" width="700" title="R.D.B">
  <br>
</p>


#### Healthy
Original:
<p align="center">
  <img src="media/4.png" width="250" title="O.O.B">
  <br>
</p>

Results:
<p align="center">
  <img src="media/5.png" width="700" title="R.O.B"
  <br>
</p>

### Model Evaluation (Binary)

<p align="center">
  <img src="media/6.png" width="700" title="Binary Evaluation"
  <br>
</p>

### Grad-Cam Visual (Multiclass)

#### Tea Algal Leaf Spot
Original:
<p align="center">
  <img src="media/7.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/8.png" width="700" title="">
  <br>
</p>

#### Brown Blight
Original:
<p align="center">
  <img src="media/9.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/10.png" width="700" title="">
  <br>
</p>

#### Grey Blight
Original:
<p align="center">
  <img src="media/11.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/12.png" width="700" title="">
  <br>
</p>

#### Helopeltis
Original:
<p align="center">
  <img src="media/13.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/14.png" width="700" title="">
  <br>
</p>

#### Red Spider
Original:
<p align="center">
  <img src="media/15.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/16.png" width="700" title="">
  <br>
</p>

#### Green Mirid Bug
Original:
<p align="center">
  <img src="media/17.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/18.png" width="700" title="">
  <br>
</p>

#### Healthy
Original:
<p align="center">
  <img src="media/4.png" width="250" title="">
  <br>
</p>

Results:
<p align="center">
  <img src="media/19.png" width="700" title="">
  <br>
</p>

### Model Evaluation (Multiclass)

<p align="center">
  <img src="media/20.png" width="700" title="Multiclass Evaluation"
  <br>
</p>

## Conclusion

## Limitation
