# Automatic-Mixed-Precision-
NVIDIA's Automatic Mixed Precision(AMP) is applied on a language model used for trigger word detection. Main aim is to find out if AMP helps the model to converge faster.

Training Dataset can be downloaded from https://drive.google.com/file/d/1---Wz0YoQ0xH6B4TP0IsUQnxRTVC9v5V/view?usp=drivesdk

XY_Train.zip can be downloaded from the link. 

You need to unzip this foldeer and put it inside the folder "Automatic-Mixed-Precision"

In the files written as "AMP ASR Trial x" we are using Automatic Mixed Precision and in the files written as "ASR Trian x" we are not using Automatic Mixed Precision.
For eg. Code is same for "ASR Trial 2" and "AMP ASR Trial 2", except "AMP ASR Trial 2" has an added line of code where Automatic Mixed Precision is being utilised.

Observations:-

1. AMP ASR Trial 1, A 5 layer language model is built from scratch and for training we are using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows "loss = 0.6885, time = 100.596"

2. ASR Trial 1, A 5 layer language model is built from scratch and for training with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows "loss = 1.2722, time = 86.03s"

3. AMP ASR Trial 2, A 5 layer language model is built from scratch and for training we are using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 32, Epochs=10" Results are as follows  "loss = 0.6788, time = 150.20s"

4. ASR Trial 2, A 5 layer language model is built from scratch and for training with the following hyperparameters "Batch Size = 32, Epochs=10" Results are as follows "loss = 1.225, time = 127.96s"

5. AMP ASR Trial 3, A pretrained model is loaded and compiled and is furthur trained with our data with using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows  "loss = 0.2833, time = 99.3s"

6. ASR Trial 3, A pretrained model is loaded and compiled and is furthur trained with our data with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows "loss = 0.2695, time = 96.67s"
