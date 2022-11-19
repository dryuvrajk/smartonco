# SMARTOnco
AI Enabled Android App for Detecting Skin Cancer, by Dr. Yuvraj Kumar (Ph.D - Artificial Intelligence)

In recent days, skin cancer is seen as one of the most Hazardous form of Cancers found in Humans. Skin cancer is found in various types such as Melanoma, Basal and Squamous cell Carcinoma among which Melanoma is the most unpredictable. The detection of Melanoma cancer in the early stage can be helpful to cure it. Computer vision can play important role in Medical Image Diagnosis and it has been proved by many existing systems.

Oncology is the study of cancer. An oncologist is a doctor who treats cancer and provides medical care for a person diagnosed with cancer. An oncologist may also be called a cancer specialist.

The field of oncology has 3 major areas based on treatments: medical oncology, radiation oncology, and surgical oncology.

Medical oncologists treat cancer using medication, including chemotherapy, immunotherapy, and targeted therapy.

Radiation oncologists treat cancer using radiation therapy, which is the use of high-energy x-rays or other particles to destroy cancer cells.

Surgical oncologists treat cancer using surgery, including removing the tumor and nearby tissue during a operation. This type of surgeon can also perform certain types of biopsies to help diagnose cancer.

### What is the role of the oncologist?

An oncologist manages a patient's care throughout the course of the disease. This starts with the diagnosis. Their role includes:

Recommending tests to determine whether a person has cancer

Explaining a cancer diagnosis, including the type and stage of the cancer

Talking about all treatment options and your treatment choice

Delivering quality and compassionate care

Helping you manage symptoms and side effects of cancer and its treatment

A person's cancer treatment plan may include more than one type of treatment, such as surgery, cancer medications, and/or radiation therapy. That means different types of oncologists and other health care providers work together to create a patient's overall treatment plan. This is called a multidisciplinary team.

Cancer care teams often include a variety of other health care professionals, including pathologists, radiologists, physician assistants, nurse practitioners, oncology nurses, social workers, pharmacists, and more. Learn about these and other possible members of a multidisciplinary team in another article on this website. Doctors from other areas of medicine can also be part of this team. For example, a dermatologist, which is a specialist in skin problems, may help treat skin cancer.

Using this app which is combined with the power of artificial intelligence, we intend to provide rapid first level self diagnosis opportunity to the medical professionals including common man. 

# SmartOnco - Project placement 

The project is mainly divided into two parts:

> TensorFlow and Keras are used to build and create a machine learning model.
> TFLite is used to deploy the model to an Android application.

Using Convolutional Neural Networks (CNN), algorithm development and model training has been done to distinguish between benign and malignant skin cancers. 

## Loading the dataset

You can use your own custom dataset. I have used the skin cancer dataset for binary classification of benign vs malignant cancer types, once done, annotation (labelling) needs to be performed. 

## Transfer Learning with TensorFlow hub:

Select the Hub/TF2 module to use, you can choose inception v3 or Mobile net. In this module, MobileNet model has been used. 

## Data Preprocessing:

Kindly Set up data generators to read images from source folders, transform them to float32 tensors, and feed them to the network (along with their labels). NOTE: data that is fed into neural networks is normally normalised in some way to make it easier for the network to process.

For this project, data has been preprocessed including images by converting the pixel values to [0, 1] range (all values are in the [0, 255] range). NOTE: The input data must be scaled to 224×224 pixels as an input, as specified by the networks. You can choose whether or not to use image AUGMENTATION option.

## Building the model:

It’s as simple as using the Hub module to layer a linear classifier on top of the feature extractor. You may start with a non-trainable feature extractor for speed, but you may enable fine-tuning for more accuracy, although training the model generally takes long time which may be further be reduced if the computing infrastructure is advanced as compared to normal GPU. 

## Training the Model:

Each step has to be validated by training the model with the validation dataset. I have been able to achieve close to 98% accuracy after 21 epochs, but fine-tuning can increase this to achieve 99.99% Accuracy. 

# Files

Download all the files in a folder. Install Winrar and unzip the files to view master folder.

# AI Model

Model is already trained using CNN. The model and the ipynb code is in Training folder.

# Android App

I am not an Android Developer. The app could be buggy or may not work at all. If you want to work on this app, you may import the project, look at the code to understand it better, and further look at the AI integration on how it is done.

TFLite has been used to build this end-to-end Android application.

### Adding TFLite model to the Android Project

First — load the model in the Android project, model.tflite (not included in this repo upload) and labels.txt into assets/ directory. The file model.tflite is the result of the model training done using jupyter notebook (anaconda 3). Add TFLite dependency to app/build.gradle file.

# Sample images used for Model Training

Benign - 30 Images

Malignant - 27 Images 

## Proof of Concept 

### Benign - 99% confidence 

![Screenshot](7.jpg)

### Malignant - 99% confidence

![Screenshot](8.jpg)

### App UI Sample

![Screenshot](image-skin-app.png)

## Suggestions and inputs (if any) 

Any suggestions or cowork opportunity is welcome to enhance the application. 
