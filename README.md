# CU-Fintech202211-DeepLearning
# Neural Network using Keras

In this program Tensorflow library is used to create Deep Learning models on application data of startups to predict their likelihood of success.

## Technologies
This program uses Tensorflow which has several dependencies most of which are installed by default in the conda environment.

---
## Installation Guide

To install TensorFlow use the following command in the dev environment.

```python
pip install --upgrade tensorflow
```
To verify installation use

```python
python -c "import tensorflow as tf;print(tf.__version__)"
```

The output of this command should show version 2.0.0 or higher.

Keras is a popular deep learning framework that serves as a high-level API for TensorFlow. Keras is now included with TensorFlow 2.0. So, run the following command to verify that the package is available:

```python
python -c "import tensorflow as tf;print(tf.keras.__version__)"
```
The output should show version 2.2.4-tf or later.

---

## Usage

This program uses application data to predict the likelihood of success of a startup. In order to assess the likely, deep neural network is used.

The initial DNN is set up with 2 layers with default settings to set a benchmark assessment of the model performance. In the first iteration there are a total of 6786 parameters in the first layer and a total of 8527 parameters. 

```
                                        Model: "sequential"
                                        _________________________________________________________________
                                         Layer (type)                Output Shape              Param #   
                                        =================================================================
                                         dense (Dense)               (None, 58)                6786      

                                         dense_1 (Dense)             (None, 29)                1711      

                                         dense_2 (Dense)             (None, 1)                 30        

                                        =================================================================
                                        Total params: 8,527
                                        Trainable params: 8,527
                                        Non-trainable params: 0
                                        _________________________________________________________________
```

Using 20 epochs the DNN arrives at a `Loss: 0.5523096323013306` and `Accuracy: 0.7265306115150452`


There are two additional iterations of the model. In the second iteration a 2nd input layer is added to the model. Keeping the epochs constant at 20 no significant improvment in model performance was noted with `Loss: 0.5518964529037476` and `Accuracy: 0.7292128205299377`.

Further iteration, uses the initial 2 layer DNN model but adds additional epochs and as a result a slight improvement in model `Loss: 0.5687777996063232` and `Accuracy: 0.7300291657447815`. This indicates that the 2 layer DNN with additional epoch has the capacity to performan better over higher iteration in the given data.

---

## Contributors


Kunal Srinivasan

---

## License

2022 edX Bootcamps 