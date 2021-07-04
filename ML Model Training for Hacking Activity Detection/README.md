## Machine Learning Model Training for Hacking Activity Detection

#### Project Overview
<p>This project aims to train a machine learning model to automatically detect the computer hacking activities. The whole project is divided into two parts of work. While first part of work aims to train the 2 prediction model for given data, the second part of work aims to create a proof-of-concept streaming application to demonstrate the integration of machine learning model, Kafka and Spark streaming and create visualisation for monitoring purpose</p>

<p> The first part of work includes `data cleaning`,`data exploration`, `feature selection`, `pipline establishent`, `Model Training`, `Model Performance Analysis`, `AUC Calculating and Ploting` etc </p>

<p>The secont part of work includes `Data Producer Creation (for simulation purpose)`, `Data consumer creation to visulize the Data Stream`, `Streaming Application Creation which integrates the ML model`, `Data Transformation for dirty data from stream`, `Stream Data Persist`, `Prediction on Stream Data using the ML model`, `Aggregation for prediction result` etc</p>

#### Dataset Info
<p>Four data files recorded from Linux systems are provided, which captures information
relating to the memory activity, and process activity. They are a subset of the Internet of
Things dataset collected by Dr. Nour Moustafa, from IoT devices, Linux systems, Windows
systems, and network devices. For more detailed information on the dataset, please refer to
the Metadata file included in the assignment dataset or from the website below
https://ieee-dataport.org/documents/toniot-datasets .</p>
<p>In this project, the memory activity and the process activity data are provided
separately, without explicit linkage or computer ID to link up memory and process. For each
data, there is a binary label and a multi-class label, one for indicating whether the activity is
an attack or not, and the other for indicating which kind of attack the activity is under.</p>

#### Objective
<p>The StopHacking company requires us to build separate models for the memory activity and the process activity. Each activity needs a model for a binary classification predicting
whether it is an attack or not, as shown in use case 1 & 2 below. To build the binary
classification model, use the column “attack” as your label in the model (label 0 as
non-attack event, and label 1 as attack event). You can select any columns as features from
each activity data, except “attack” or “type”.</p>
| 1    | Process activity - attack or not Binary classification | Binary classification |
| ---- | ------------------------------------------------------ | --------------------- |
| 2    | Memory activity - attack or not                        | Binary classification |

#### Architecture

![arch.PNG](https://github.com/Shain001/BigDataProcess-Machine-Learning-Kafka-Stream/blob/main/ML%20Model%20Training%20for%20Hacking%20Activity%20Detection/arch.PNG?raw=true)

