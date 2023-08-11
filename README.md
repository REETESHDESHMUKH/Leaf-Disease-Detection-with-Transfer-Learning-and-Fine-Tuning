# Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning
## Abstract
Leaf disease detection will replace the manual method, which is time-consuming as we have to go through every leaf manually and it also requires expertise. This paper uses image pre-processing techniques such as **data augmentation** to process the image before passing it through the model for feature extraction. **Data augmentation** is used to get high accuracy and efficiency. This paper discusses our CNN model which we built to detect leaf diseases and recommend treatment on basis of confidence level. Further, we have used this model to detect leaf diseases on other leaves like tomatoes using the concept of **Transfer learning** and **Fine tuning**.

## Dataset
This dataset contains 10 directories denoting diseases like Potato Early blight, Potato healthy etc.
Total files : 10000 files
Each disease : atleast 1000 files.
Dataset should be bifurcated into 3 subsets, namely:
**• Training [80%]:** Dataset to be used while training.
**• Validation [10%]:** Dataset to be tested against while
training.
**• Test [10%]:** Dataset to be tested against after we trained
a model

## Pre-processing
**• Auto-Tune:** helps to pick optimal part of dataset for our
tensor flow model.
Shuffle: [1000]
**• Resize and Rescaling:** so basically by default layer
output float hence its necessary to resize and rescale it
using builtin functions of keras.
Resize: [256x256]
Rescale: [1./255]
**• Data augmentation:** By using data augmentation, we
hope to improve the model’s generalizability.
Random FLip : ”horizontal and vertical”
Random Rotation : 20 degree.

## Results
### Detection
<img width="269" alt="image" src="https://github.com/REETESHDESHMUKH/Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning/assets/76653982/cfff2669-d86c-4fd7-a35c-df5f02b45a2a">

### A. Data Augmentation
**Before :** 
<img width="266" alt="image" src="https://github.com/REETESHDESHMUKH/Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning/assets/76653982/87f3a781-2620-474b-ba2d-7dbe5a94553c">

The accuracy after applying data augmentation comes out to
be 98.84%. An improvement of 3.64% in accuracy can be
observed here.

**After :**
<img width="248" alt="image" src="https://github.com/REETESHDESHMUKH/Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning/assets/76653982/f9272427-e99b-40fc-bdce-4644783fe136">

### B. Fine Tuning 
**Before :**
<img width="245" alt="image" src="https://github.com/REETESHDESHMUKH/Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning/assets/76653982/3a00fefa-a879-4ace-bb05-dca43199a269">

We apply fine-tuning on the model and then test it on tomato
leaves. We were able to increase the accuracy further to
94.12%

**After :**
<img width="248" alt="image" src="https://github.com/REETESHDESHMUKH/Leaf-Disease-Detection-with-Transfer-Learning-and-Fine-Tuning/assets/76653982/0cb226ae-503b-41e8-a12c-1d352c01efdd">

## Conclusion
We were successfully able to build a leaf disease detection
system using the concepts of convolutional neural networks.
The model was able to give an accuracy of 98.84% when
trained on the whole data set. The transfer learning with finetuning was also successfully executed as we were able to
detect disease on tomato leaves by training the model on potato
leaves with an accuracy of 94.12%.
We still need to work on developing a better treatment
recommendation system, where we have to combine data
related to nitrogen, phosphorous, and potassium content with
diseases, to give more accurate treatment because by knowing
the contents of the soil we will be able to predict the lacking
contents to predict a better solution for treatment. So, the
data we have as of now is somewhat insufficient to provide a
better treatment solution.
